# Syndra Pet Brief

Source patch: 16.9.1
Champion id: Syndra
Display name: Syndra
Pet package id: lol-syndra

## Reference Pack

- Riot official page: https://www.leagueoflegends.com/en-us/champions/syndra/
- Official splash: https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Syndra_0.jpg
- Official loading crop: https://ddragon.leagueoflegends.com/cdn/img/champion/loading/Syndra_0.jpg
- Model viewer: https://modelviewer.lol/model-viewer?id=134000
- Local references: `references/syndra/ddragon-syndra-splash.jpg`, `references/syndra/ddragon-syndra-loading.jpg`, `references/syndra/ddragon-syndra-icon.png`
- Notes from visual research: `references/syndra/reference-notes.md`

## Identity

- Core silhouette: compact chibi dark sovereign mage with a huge silver-white hair sweep, angular black-purple crown, jagged high shoulder armor, dark violet bodysuit, and one small dark sphere held close.
- Palette: black and deep violet clothing, silver-white hair, magenta-violet armor glints, tiny hard-edged purple magic attached to hands or sphere.
- Face/personality: severe, proud, controlled, slightly floating posture; small sharp eyes and dark lips.
- Must-keep prop or body feature: the crown, silver-white hair, jagged shoulder armor, and at least one close dark sphere must stay readable in every row.
- Simplify/remove: do not use giant orbiting spheres, huge black holes, detached star fields, loose purple trails, enemy targets, spell labels, or detailed armor filigree.

## Ability Mapping

| Ability | Spell name | Codex row | Pet-sized visual cue | Forbidden interpretation |
| --- | --- | --- | --- | --- |
| Q | Dark Sphere | `waving` | one hand lifts a small dark sphere close to the palm with a tiny attached violet rim | giant orb, detached projectile trail, multiple loose spheres, area marker, or skill icon |
| W | Force of Will | `waiting` | calm levitation stance with the close sphere tucked above both hands as if held by will | thrown minion, enemy object, UI arrow, distant floating ball, or large telekinesis beam |
| E | Scatter the Weak | `jumping` | sharp upward recoil pose with the close sphere nudged forward against the body silhouette | wide cone blast, stun symbols, speed lines, detached shockwave, or enemy target |
| R | Unleashed Power | `review` | focused sovereign casting pose with two or three tiny attached dark spheres clustered tight around the hands/body | barrage across the frame, separate orbiting planets, enemy champion, execution marker, or full-screen void |

## Prompt Notes

- Base pet prompt: A tiny chibi Codex digital pet version of Syndra, proud dark sovereign mage, huge flowing silver-white hair, angular black-purple crown, sharp dark eyes, dark violet bodysuit, jagged high shoulder armor, one small dark purple sphere held close to her hands, tiny hard-edged violet magic attached to the sphere, compact floating stance, chunky readable silhouette, pixel-art-adjacent flat cel shading, thick dark outline, transparent-friendly solid green chroma-key background.
- Row identity lock: keep the same silver-white hair mass, angular crown, dark violet bodysuit, jagged shoulder armor, sharp proud face, compact floating stance, and close dark sphere in every row.
- Chroma-key risk: avoid purple, blue, black, or white chroma backgrounds; use flat saturated green and keep all magic opaque, hard-edged, tiny, and attached to the sphere or body.
- Running-left mirror decision: likely safe only if the generated run keeps the sphere, crown, and hair as non-text asymmetric fantasy forms; inspect `running-right` before mirroring.

## QA Checklist

- [x] Reference Pack 已查并写入 brief。
- [x] Same silhouette and palette across all rows.
- [x] Q row reads as Dark Sphere without text, detached trails, or giant orb clutter.
- [x] W row reads as Force of Will without minions, arrows, or distant floating props.
- [x] E row reads as Scatter the Weak without cone blasts, stun symbols, or enemy targets.
- [x] R row reads as Unleashed Power without full-frame barrage or separate orbiting planets.
- [x] Failed row is an app error/reaction state, not confused with Q/W/E/R.
- [x] Contact sheet has no cropped bodies, white boxes, guide marks, shadows, or loose particles.
- [x] `qa/review.json` has no errors.
- [x] `final/validation.json` has no errors.
