# K'Sante Pet Brief

Source patch: 16.9.1
Champion id: KSante
Display name: K'Sante
Pet package id: lol-ksante

## Reference Pack

- Official champion page: https://www.leagueoflegends.com/en-us/champions/k-sante/
- Official splash: `references/ksante/ddragon-ksante-splash.jpg`
- Official loading crop: `references/ksante/ddragon-ksante-loading.jpg`
- Official square icon: `references/ksante/ddragon-ksante-icon.png`
- DDragon champion data: `data/ddragon/16.9.1/champions/KSante.json`

## Identity

- Core silhouette: compact chibi Nazumah warrior with white swept dreadlock-like hair, broad dark-skinned face and body, teal-and-gold armor plates, cream cloth wraps, and two oversized ntofo tonfa/blade weapons held close.
- Palette: dark brown skin, white hair, turquoise/teal armor, warm gold trim, cream wraps, muted stone-gray weapon mass, and tiny amber highlights only when attached to the body or ntofos.
- Face/personality: defiant, proud, protective hunter energy; stern focused eyes and squared stance without turning into a generic knight, monk, or armored barbarian.
- Must-keep prop or body feature: both ntofo weapons must remain readable and physically attached to K'Sante's hands/body silhouette in every row.
- Simplify/remove: remove fine armor engravings, long weapon inscriptions, background oasis/sand, enemies, walls, broad shockwaves, dust trails, large shields, and loose teal/gold particles.

## Ability Mapping

| Ability | Spell name | Codex row | Pet-sized visual cue | Forbidden interpretation |
| --- | --- | --- | --- | --- |
| Q | Ntofo Strikes | `waving` | one compact ntofo wind-up or short forward strike with both weapons still touching the silhouette | Shockwave projectile, three-stack icon, pulled enemy, long slash arc, impact mark, or text |
| W | Path Maker | `waiting` | braced charge stance with crossed ntofos tucked close against the body | Long dash trail, wall collision, enemy knockback, floor dust, shield bar, or scenery |
| E | Footwork | `jumping` | short evasive hop/step with a tiny attached shield glint on the body or weapon | Detached shield bubble, ally target, speed lines, afterimage, dust, or floor shadow |
| R | All Out | `review` | intense transformed stance with one ntofo blade opened/extended close to the body | Enemy launch, wall break, huge aura, full transformation cutscene, floating buff icon, or cinematic background |

## Prompt Notes

- Base pet prompt: A tiny chibi Codex digital pet version of League of Legends K'Sante, the Pride of Nazumah, dark-skinned proud warrior, white swept dreadlock-like hair, teal-and-gold armor, cream cloth wraps, two oversized stone-and-gold ntofo tonfa/blade weapons held close, stern protective face, chunky readable whole-body silhouette, pixel-art-adjacent flat cel shading, thick dark outline, transparent-friendly solid chroma-key background.
- Row identity lock: keep the same white hair shape, dark brown skin, teal-gold armor plates, cream wraps, stern eyes, compact warrior proportions, and paired oversized ntofo weapons in every row.
- Chroma-key risk: K'Sante uses teal, gold/yellow, cream, and white; use a flat saturated magenta background and keep all teal/gold cues opaque, hard-edged, small, and physically attached.
- Running-left mirror decision: likely safe only if both ntofos have no readable markings and the pose does not depend on handedness after `running-right`; inspect before mirroring because the paired weapons and stance can make asymmetry noticeable.

## QA Checklist

- [ ] Reference Pack 已查并写入 brief。
- [ ] Same silhouette and palette across all rows.
- [ ] Reads as League of Legends K'Sante, not a generic armored warrior, knight, monk, or barbarian.
- [ ] White hair, dark skin, teal-gold armor, cream wraps, and paired ntofos stay readable.
- [ ] Q row reads as Ntofo Strikes without text, detached shockwaves, or enemies.
- [ ] W row reads as Path Maker without walls, dust trails, or detached shield bars.
- [ ] E row reads as Footwork without speed lines, afterimages, or loose shield bubbles.
- [ ] R row reads as All Out without enemies, wall breaks, huge aura, or buff icons.
- [ ] Failed row is an app error/reaction state, not confused with Q/W/E/R.
- [ ] Contact sheet has no cropped bodies, white boxes, guide marks, shadows, or loose particles.
- [ ] `qa/review.json` has no errors.
- [ ] `final/validation.json` has no errors.
