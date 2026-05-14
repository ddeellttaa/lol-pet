# Rek'Sai Pet Brief

Source patch: 16.9.1
Champion id: RekSai
Display name: Rek'Sai
Pet package id: lol-reksai

## Reference Pack

- Riot official page: https://www.leagueoflegends.com/en-us/champions/reksai/
- Official splash: `references/reksai/ddragon-reksai-splash.jpg`
- Official loading crop: `references/reksai/ddragon-reksai-loading.jpg`
- Champion icon: `references/reksai/ddragon-reksai-icon.png`
- Model viewer: https://modelviewer.lol/model-viewer?id=421000
- Local model screenshot: `references/reksai/modelviewer-421000.png`
- Notes from visual research: `references/reksai/reference-notes.md`

## Identity

- Core silhouette: compact quadrupedal Void burrower with a low predatory stance, tall central forehead horn, broad crescent-like foreclaws, hunched back armor plates, purple side mandibles, pale lower fangs, and dark rear claws.
- Palette: deep void purple body, saturated cyan-blue carapace plates, magenta horn and mandible accents, dark indigo claws, and tiny pale yellow-white teeth.
- Face/personality: eyeless underground apex predator; hungry, alert, and alien, but simplified into a readable Codex pet.
- Must-keep prop or body feature: central horn, sweeping side mandibles, huge foreclaws, low four-limbed body, and blue-purple Void palette must stay readable in every row.
- Simplify/remove: remove fine armor seams, background sand, tunnels as separate scenery, loose void mist, large shockwaves, shadows, UI marks, spell icons, and any skin-specific alternate colors.

## Ability Mapping

| Ability | Spell name | Codex row | Pet-sized visual cue | Forbidden interpretation |
| --- | --- | --- | --- | --- |
| Q | Queen's Wrath / Prey Seeker | `waving` | three-frame close claw swipe or head-snap pose using the attached foreclaws and mandibles | Detached slash rings, floating projectiles, reveal icons, enemies, or ranged missiles |
| W | Burrow / Un-burrow | `waiting` | low crouched burrow-ready posture with the horn and back plates dipping down, then lifting slightly | Separate tunnel holes, sand piles, dust clouds, floor marks, or underground cross-sections |
| E | Furious Bite / Tunnel | `jumping` | compact bite-lunge with mandibles open and foreclaws tucked close | Separate target, tunnel entrance prop, speed lines, blood, damage numbers, or loose earth chunks |
| R | Void Rush | `review` | focused pouncing stance with body compressed forward and a tiny attached hard-edged purple energy accent on the horn or chest | Huge aura, teleport ring, target mark, enemy silhouette, shadow trail, or detached void cloud |

## Prompt Notes

- Base pet prompt: A tiny chibi Codex digital pet version of League of Legends Rek'Sai, the Void Burrower: low quadrupedal alien Void predator with a tall central magenta forehead horn, sweeping purple side mandibles, broad blue crescent foreclaws, hunched cyan-blue armor plates, dark indigo rear claws, pale lower fangs, eyeless face, compact four-limbed body, deep purple and cyan Void palette. Pixel-art-adjacent flat cel shading, thick dark outline, limited palette, no text, no Riot logo, no scenery.
- Row identity lock: keep the same central horn, side mandibles, huge foreclaws, low quadrupedal body, hunched back plates, pale fangs, and blue-purple palette in every row.
- Chroma-key risk: Rek'Sai uses purple, magenta, blue, and cyan, so use a flat saturated green background and avoid green anywhere in the pet.
- Running-left mirror decision: likely safe only if the row has no side-specific lighting or asymmetrical markings; inspect `running-right` before mirroring.

## QA Checklist

- [ ] Reference Pack checked and written into brief.
- [ ] Same silhouette and palette across all rows.
- [ ] Clearly reads as League of Legends Rek'Sai, not a generic dragon, crab, beetle, dog, or dinosaur.
- [ ] Central horn, side mandibles, huge foreclaws, low quadrupedal body, and pale fangs remain readable.
- [ ] Q row reads as Queen's Wrath / Prey Seeker without text or detached icons.
- [ ] W row reads as Burrow / Un-burrow without text or detached icons.
- [ ] E row reads as Furious Bite / Tunnel without text or detached icons.
- [ ] R row reads as Void Rush without text or detached icons.
- [ ] Failed row is an app error/reaction state, not confused with Q/W/E/R.
- [ ] Contact sheet has no cropped bodies, white boxes, guide marks, shadows, or loose particles.
- [ ] `qa/review.json` has no errors.
- [ ] `final/validation.json` has no errors.
