# 英雄联盟全英雄 Codex Pet 生产计划

**目标：** 为英雄联盟每个英雄制作一个 Codex 自定义 pet。每只 pet 都要保持英雄辨识度，并在固定动画行里体现该英雄的 Q、W、E、R 四个技能。

**当前基线：** 2026-05-11 查询 Riot Data Dragon，最新版本为 `16.9.1`，`champion.json` 中共有 `172` 个英雄。这只是当前快照；每一轮批量生产前都要重新刷新版本和英雄数量。

**每个英雄的最终产物：**

```text
${CODEX_HOME:-$HOME/.codex}/pets/lol-<champion-id>/
├── pet.json
└── spritesheet.webp
```

## 1. 信息源

英雄清单、英雄 ID、称号、被动、Q/W/E/R 技能名、技能描述、英雄头像、技能图标都以 Riot Data Dragon 为准，不手填维护。

常用端点：

```bash
# 最新 Data Dragon 版本列表。
curl -fsSL https://ddragon.leagueoflegends.com/api/versions.json

# 某个地区当前使用的版本；需要贴近正式服时参考这个。
curl -fsSL https://ddragon.leagueoflegends.com/realms/na.json

# 指定版本的英雄索引。
curl -fsSL https://ddragon.leagueoflegends.com/cdn/<version>/data/en_US/champion.json

# 单个英雄完整数据。
curl -fsSL https://ddragon.leagueoflegends.com/cdn/<version>/data/en_US/champion/Aatrox.json

# 英雄头像、被动图标、技能图标。
https://ddragon.leagueoflegends.com/cdn/<version>/img/champion/Aatrox.png
https://ddragon.leagueoflegends.com/cdn/<version>/img/passive/<passive-full-filename>
https://ddragon.leagueoflegends.com/cdn/<version>/img/spell/<spell-full-filename>
```

默认使用 `en_US` 作为规范数据源，因为技能名和 champion id 最稳定。后续如果要做中文目录，可以额外加本地化展示名，但 pet id、数据版本和技能映射仍然绑定 Riot 的 canonical champion id。

## 2. Fan Project 与版权边界

这个项目按个人、非商业 fan project 处理。

必须遵守：

- 不声明 Riot 官方背书或合作。
- 不用 Riot logo 做项目品牌。
- 不出售 pet 包，也不打包成商业产品。
- 原始 Riot 资源只做可再生成缓存，不作为主要仓库资产长期堆积。
- 对外分享目录时，保留可见声明。

建议声明：

```text
This fan project was created under Riot Games' "Legal Jibber Jabber" policy using assets owned by Riot Games. Riot Games does not endorse or sponsor this project.
```

仓库里优先保存：生成脚本、manifest、brief、prompt、QA 结果、pet 元数据。Riot 原图、技能图标、splash 等资源可以从 Data Dragon 重建，除非确实需要留一份本地缓存用于可复现生产。

## 3. Codex Pet 固定规格

Codex pet 使用固定 sprite atlas：

| 项目 | 值 |
| --- | --- |
| Atlas 尺寸 | `1536x1872` |
| 网格 | 8 列 x 9 行 |
| 单格 | `192x208` |
| 背景 | 透明 |
| 安装文件 | `pet.json`、`spritesheet.webp` |

固定动画行：

| 行 | Codex 状态 | 使用帧数 | 本项目用途 |
| --- | --- | ---: | --- |
| 0 | `idle` | 6 | 核心英雄轮廓，第一帧也要适合 reduced-motion 静态显示 |
| 1 | `running-right` | 8 | 向右移动，体现英雄步态、武器或身体重心 |
| 2 | `running-left` | 8 | 向左移动；只有在视觉语义安全时才镜像 |
| 3 | `waving` | 4 | Q 技能表现 |
| 4 | `jumping` | 5 | E 技能表现 |
| 5 | `failed` | 8 | Codex 错误/失败反应，不占 QWER |
| 6 | `waiting` | 6 | W 技能表现 |
| 7 | `running` | 6 | 原地移动循环，强化英雄动作身份 |
| 8 | `review` | 6 | R 技能表现 |

Codex 的行名是固定的，所以 QWER 需要映射到可用状态里。默认映射如下：

| 技能 | 动画行 | 表现方向 |
| --- | --- | --- |
| Q | `waving` | 快速招式、武器起手、投射物起手、手势施法 |
| W | `waiting` | 架势、防御、蓄力、召唤、自我强化、第二魔法主题 |
| E | `jumping` | 位移、跳跃、冲刺、落点、技巧动作、短促爆发 |
| R | `review` | 终极技能姿态、变身提示、大招能量感，但必须保持小而清楚 |

如果某个英雄的技能不适合默认含义，也不要换行；保留 Q/W/E/R 对应的四个行位，在 brief 里写清楚这个英雄的解释。例如某英雄 W 是位移、E 是护盾，那么 `waiting` 可以显示护盾，`jumping` 可以显示 E 的非位移特征。

## 4. 视觉风格规则

目标不是把 splash art 缩成小图，而是把英雄转译成 Codex 数字宠物。

应该使用：

- 紧凑 chibi 比例。
- 粗而易读的轮廓。
- 类像素的深色 1-2 px 描边感。
- 有限制的调色盘。
- 平面 cel shading。
- 小短肢体和明确表情。
- 一到两个英雄锚点：武器、发型、面具、身体结构、代表色、标志性道具。

避免：

- 文字、字母、伤害数字、UI 面板、气泡、技能标签。
- Riot logo 或英雄名排版。
- splash art 级别的复杂服饰。
- 离体粒子、独立星星、阴影、辉光、速度线、尘土、拖尾、运动弧线。
- 在 `192x208` 中看不清的小饰品。
- 把技能图标原样悬浮在 pet 旁边。

允许的小特效必须满足：贴住或覆盖 pet 轮廓、硬边、非透明软光、在单格内完整可见、不会被误当成独立 sprite。优先用姿势和轮廓表达技能，不靠漂浮特效堆信息。

## 5. 每个英雄的 Brief 模板

每个英雄生成前先写 brief，路径：

```text
briefs/<champion-id>.md
```

模板：

```markdown
# <Champion Name> Pet Brief

Source patch: <Data Dragon version>
Champion id: <ChampionId>
Display name: <Champion Name>
Pet package id: lol-<champion-id-lowercase>

## Identity

- Core silhouette:
- Palette:
- Face/personality:
- Must-keep prop or body feature:
- Simplify/remove:

## Ability Mapping

| Ability | Spell name | Codex row | Pet-sized visual cue | Forbidden interpretation |
| --- | --- | --- | --- | --- |
| Q | <spell> | `waving` | <one compact cue> | <what would clutter or misread> |
| W | <spell> | `waiting` | <one compact cue> | <what would clutter or misread> |
| E | <spell> | `jumping` | <one compact cue> | <what would clutter or misread> |
| R | <spell> | `review` | <one compact cue> | <what would clutter or misread> |

## Prompt Notes

- Base pet prompt:
- Row identity lock:
- Chroma-key risk:
- Running-left mirror decision:

## QA Checklist

- [ ] Same silhouette and palette across all rows.
- [ ] Q row reads as the Q ability without text or detached icons.
- [ ] W row reads as the W ability without text or detached icons.
- [ ] E row reads as the E ability without text or detached icons.
- [ ] R row reads as the R ability without text or detached icons.
- [ ] Failed row is an app error/reaction state, not confused with Q/W/E/R.
- [ ] Contact sheet has no cropped bodies, white boxes, guide marks, shadows, or loose particles.
- [ ] `qa/review.json` has no errors.
- [ ] `final/validation.json` has no errors.
```

Brief 的重点是做取舍。每个技能只选一个 pet 尺寸下能看懂的 cue，不追求复刻完整技能逻辑。

## 6. 生产流程

### 6.1 刷新数据

拉取当前 Data Dragon 版本、英雄索引、单英雄 JSON，放到版本化缓存：

```text
data/ddragon/<version>/
├── champion.json
└── champions/
    ├── Aatrox.json
    ├── Ahri.json
    └── ...
```

生成规范化 manifest：

```text
data/manifests/champions-<version>.json
```

manifest 最少字段：

```json
{
  "version": "16.9.1",
  "champions": [
    {
      "id": "Aatrox",
      "key": "266",
      "name": "Aatrox",
      "title": "the Darkin Blade",
      "spells": {
        "Q": { "name": "The Darkin Blade", "image": "AatroxQ.png" },
        "W": { "name": "Infernal Chains", "image": "AatroxW.png" },
        "E": { "name": "Umbral Dash", "image": "AatroxE.png" },
        "R": { "name": "World Ender", "image": "AatroxR.png" }
      },
      "passive": { "name": "Deathbringer Stance", "image": "Aatrox_Passive.png" }
    }
  ]
}
```

### 6.2 生成 Brief

从 manifest 为每个英雄生成 `briefs/<champion-id>.md`。

规则：

- 每个 Q/W/E/R 只选一个可读 cue。
- 优先用英雄姿势、轮廓和道具表达，不用大面积粒子。
- 技能颜色只有在足够标志性且不影响 chroma-key 时才写入 prompt。
- 多形态英雄默认用 base skin 最常见形态；如果 R 是变身，可以在 `review` 行做小幅终极形态提示。
- 复杂机制写成解释，不要硬塞进 192x208 小格。

### 6.3 先做 Pilot Batch

全量生产前先做 5 个试点：

| 英雄 | 试点价值 |
| --- | --- |
| Garen | 近战轮廓简单，Q/W/E/R 映射直接 |
| Annie | 小体型法师，火焰和召唤 cue 容易检查 |
| Ahri | 尾巴、魅惑、位移，测试多尾轮廓稳定性 |
| Jinx | 武器复杂，测试大枪/火箭炮在 pet 尺寸下是否可读 |
| Yasuo | 风和斩击容易生成离体特效，适合测试限制规则 |

5 个试点必须都能安装进 Codex，并且 contact sheet 通过视觉审查，才进入批量生产。

### 6.4 生成单个 Pet

使用已安装的 `hatch-pet` skill。父进程负责 manifest、记录 imagegen 结果、repair、finalize 和最终包写入；base 生成完成后，行图生成按 `hatch-pet` 规范交给子 agent 并行。子 agent 只负责生成并返回原始 `$CODEX_HOME/generated_images/.../ig_*.png` 路径，不修改 manifest、不复制 decoded 文件、不 finalize。

准备 run：

```bash
SKILL_DIR="${CODEX_HOME:-$HOME/.codex}/skills/hatch-pet"
CHAMPION_ID="<ChampionId>"
PET_ID="lol-$(printf '%s' "$CHAMPION_ID" | tr '[:upper:]' '[:lower:]')"

python "$SKILL_DIR/scripts/prepare_pet_run.py" \
  --pet-name "LoL <Champion Name>" \
  --pet-id "$PET_ID" \
  --display-name "LoL <Champion Name>" \
  --description "A Codex pet inspired by <Champion Name>, with Q/W/E/R ability cues." \
  --output-dir "$PWD/runs/<version>/$CHAMPION_ID" \
  --pet-notes "$(cat briefs/$CHAMPION_ID.md)" \
  --force
```

检查待生成 job：

```bash
python "$SKILL_DIR/scripts/pet_job_status.py" \
  --run-dir "$PWD/runs/<version>/$CHAMPION_ID"
```

推荐生成顺序：

1. 生成并记录 base image。
2. 先生成 `idle` 和 `running-right`，确认身份和步态没有跑偏。
3. 只有在英雄左右镜像不会破坏武器、标记、方向语义时，才镜像 `running-left`。
4. 生成 Q/W/E/R 映射行：`waving`、`waiting`、`jumping`、`review`。
5. 生成 app 支撑行：`failed`、`running`。
6. finalize 并做 QA。

如果当前环境不能使用子 agent，停止在行图生成前记录 blocker；不要静默退回串行生产，除非这次任务明确要求“不使用子 agent”或“串行生成”。

记录选中的 imagegen 输出：

```bash
python "$SKILL_DIR/scripts/record_imagegen_result.py" \
  --run-dir "$PWD/runs/<version>/$CHAMPION_ID" \
  --job-id <job-id> \
  --source /absolute/path/to/generated-output.png
```

Finalize，并固定输出包路径：

```bash
python "$SKILL_DIR/scripts/finalize_pet_run.py" \
  --run-dir "$PWD/runs/<version>/$CHAMPION_ID" \
  --package-dir "${CODEX_HOME:-$HOME/.codex}/pets/$PET_ID"
```

run 目录预期产物：

```text
runs/<version>/<champion-id>/
├── pet_request.json
├── imagegen-jobs.json
├── prompts/
├── decoded/
├── frames/frames-manifest.json
├── final/spritesheet.png
├── final/spritesheet.webp
├── final/validation.json
└── qa/
    ├── contact-sheet.png
    ├── review.json
    ├── run-summary.json
    └── videos/*.mp4
```

### 6.5 最小范围修复

验证或视觉审查失败时，先修坏掉的行，不重做整只 pet：

```bash
python "$SKILL_DIR/scripts/queue_pet_repairs.py" \
  --run-dir "$PWD/runs/<version>/$CHAMPION_ID"
```

常见问题和修复：

| 问题 | 修复策略 |
| --- | --- |
| 行之间英雄身份漂移 | 只重生成漂移行，加强 identity lock |
| Q/W/E/R cue 看不懂 | 简化成一个贴身姿势或硬边小特效 |
| 出现离体粒子、阴影、速度线 | 去掉特效，改用姿势和轮廓表达 |
| `running-left` 镜像破坏不对称武器/标记 | 不镜像，重生成 `running-left` |
| contact sheet 出现白底、裁切、guide mark | 重生成对应行，加强透明背景和 cell 边界要求 |

### 6.6 接受并入库

一只 pet 必须同时满足：

- `${CODEX_HOME:-$HOME/.codex}/pets/lol-<champion-id>/pet.json` 存在。
- `${CODEX_HOME:-$HOME/.codex}/pets/lol-<champion-id>/spritesheet.webp` 存在。
- `final/validation.json` 没有 errors。
- `qa/review.json` 没有 errors。
- contact sheet 中所有行都是同一只英雄 pet，没有物种、脸、武器、配色漂移。
- Q/W/E/R 分别能在 `waving`、`waiting`、`jumping`、`review` 中看出来。
- 没有文字、技能图标、UI 符号、离体粒子云、投影、guide mark。
- 能在 Codex Settings -> Appearance / Pets 中选中。
- `/pet` 能唤醒这只 pet。

验收后更新：

```text
catalog/pets-status.csv
docs/champion-pet-todo.md
```

`catalog/pets-status.csv` 是机器可读状态表，`docs/champion-pet-todo.md` 是人看的英雄级 TODO。以后判断“哪些英雄做了，哪些没做”，以这两份文件为准，而不是只看工程任务清单。

CSV 建议字段：

```csv
champion_id,champion_name,source_version,status,q_status,w_status,e_status,r_status,package_id,brief_path,run_dir,qa_contact_sheet,accepted_at,notes
```

整只 pet 的状态枚举：

- `planned`
- `briefed`
- `generated`
- `needs-repair`
- `accepted`
- `regenerate-after-patch`

Q/W/E/R 的状态枚举：

- `planned`
- `briefed`
- `generated`
- `needs-repair`
- `accepted`

四个技能都达到 `accepted`，并且整只 pet 通过 QA 后，英雄才算完成。Q/W/E/R 固定映射为：Q = `waving`，W = `waiting`，E = `jumping`，R = `review`。

## 7. 批量策略

按 wave 推进，避免一次性生成 172 个以后才发现风格偏了。

| Wave | 范围 | 退出条件 |
| --- | --- | --- |
| 0 | 仓库结构、数据刷新、manifest、brief 模板 | 脚本和目录存在，英雄数量记录成功 |
| 1 | 5 个 pilot 英雄 | 都能安装，QWER 可读，QA 规则稳定 |
| 2 | 20 个低复杂度英雄 | 批处理顺畅，修复率低于 25% |
| 3 | 30 个中复杂度英雄 | 道具、投射物、技能 cue 规则稳定 |
| 4 | 多形态、多单位、特殊机制英雄 | 特例规则写进文档 |
| 5 | 剩余英雄 | 全部 accepted 或明确进入 repair 队列 |
| 6 | 最终目录检查 | 当前版本每个英雄都有一个 accepted package |

复杂度分桶：

- **低复杂度：** 单一清晰轮廓、简单武器、少量特效。
- **中复杂度：** 大型武器、宠物/召唤物、投射物多、架势变化明显。
- **高复杂度：** 多形态、多武器、分身、坐骑、变身、极多细节。

高风险英雄需要更细的 brief。优先标记：Aphelios、Hwei、Jayce、Nidalee、Elise、Kayn、Shaco、LeBlanc、Naafiri、Kled、Rell、Viego、Aurelion Sol。

## 8. Repository TODO

这个章节只放工程支撑任务。真正的英雄完成情况放在：

```text
docs/champion-pet-todo.md
catalog/pets-status.csv
```

当前进度：`16.9.1` 共 `172` 个英雄，`accepted = 3`，`not accepted = 169`。已完成：Aatrox、Darius、Gragas。每完成一只 pet，就同步更新对应英雄行的 checkbox、`status`、`accepted_at` 和 notes。

- [x] 创建 `data/ddragon/` 版本化缓存目录。
- [ ] 增加数据刷新脚本：抓取最新 Data Dragon 版本、英雄索引、单英雄 JSON。
- [ ] 增加 manifest 生成脚本：输出每个英雄的 passive、Q、W、E、R 字段。
- [ ] 创建 `briefs/`，从 manifest 为每个英雄生成 brief 草稿。
- [x] 创建 `catalog/pets-status.csv`，把当前所有英雄初始化为 `planned`。
- [x] 创建 `docs/champion-pet-todo.md`，列出每个英雄 done/not done 状态。
- [ ] 写 Garen pilot brief。
- [ ] 写 Annie pilot brief。
- [ ] 写 Ahri pilot brief。
- [ ] 写 Jinx pilot brief。
- [ ] 写 Yasuo pilot brief。
- [ ] 用 `hatch-pet` 生成五个 pilot pet。
- [ ] 一起审查 pilot contact sheets，并更新视觉规则。
- [ ] 增加 package QA 小脚本：检查 accepted 包含 `pet.json` 和 `spritesheet.webp`。
- [ ] 增加 catalog validator：确保当前 manifest 每个英雄都正好有一条状态记录。
- [ ] 分批生成低复杂度英雄，每批 10-20 个。
- [ ] 分批生成中复杂度英雄，每批 10-20 个。
- [ ] 高复杂度英雄单个或小批量生成。
- [ ] 对所有 accepted pet 跑最终 package 校验。
- [ ] 写使用说明：如何在 Codex 中安装、选择、唤醒生成的 pet。

## 9. 单只 Pet TODO

每个英雄都按这个 checklist 走：

- [ ] 刷新或确认 Data Dragon source version。
- [ ] 确认 champion id、display name、passive、Q/W/E/R 技能数据。
- [ ] 写或重生成 `briefs/<champion-id>.md`。
- [ ] 选择一个最重要的英雄身份视觉锚点。
- [ ] 为 Q、W、E、R 各选择一个紧凑 cue。
- [ ] 运行 `prepare_pet_run.py`。
- [ ] 生成并记录 base image。
- [ ] 生成并检查 `idle`。
- [ ] 生成并检查 `running-right`。
- [ ] 判断 `running-left` 是否可以镜像。
- [ ] 生成或派生 `running-left`。
- [ ] 生成 Q 行：`waving`。
- [ ] 生成 W 行：`waiting`。
- [ ] 生成 E 行：`jumping`。
- [ ] 生成 R 行：`review`。
- [ ] 生成 `failed`。
- [ ] 生成 `running`。
- [ ] 运行 `finalize_pet_run.py`。
- [ ] 检查 `qa/contact-sheet.png`。
- [ ] 检查 `qa/videos/*.mp4`。
- [ ] 确认 `qa/review.json` 没有 errors。
- [ ] 确认 `final/validation.json` 没有 errors。
- [ ] 如果有失败行，按最小范围 repair。
- [ ] 安装到 `${CODEX_HOME:-$HOME/.codex}/pets/lol-<champion-id>/`。
- [ ] 在 Codex Settings -> Appearance / Pets 里选择。
- [ ] 用 `/pet` 唤醒。
- [ ] 更新 `catalog/pets-status.csv`。
- [ ] 更新 `docs/champion-pet-todo.md`。

## 10. 风格漂移控制

每 accepted 20 只 pet，做一次 contact sheet wall review：

- 是否都还是 Codex pet 风格，而不是 splash art 缩略图？
- Q/W/E/R 四行在不同英雄之间的用途是否一致？
- R 行是否越来越吵、越来越像大面积特效？
- 投射物英雄是否过度使用离体粒子？
- 武器英雄是否过高、过宽或容易裁切？
- 调色盘是否接近 chroma key，导致透明抠图风险？

如果出现漂移，先更新 brief 和本生产计划，再修受影响的行。不要因为风格规则小调整就重做所有已验收 pet；只有当可读性或 Codex app 适配性受影响时才回炉。

## 11. 参考资料

- Reddit Codex pet 流程：<https://www.reddit.com/r/codex/comments/1t2rbbh/a_simple_guide_to_create_a_custom_pet_in_codex/>
- Riot Data Dragon 文档：<https://developer.riotgames.com/docs/lol#data-dragon>
- Riot fan-project policy：<https://www.riotgames.com/en/legal>
- 本地 `hatch-pet` skill：`${CODEX_HOME:-$HOME/.codex}/skills/hatch-pet/SKILL.md`
