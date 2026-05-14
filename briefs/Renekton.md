# Renekton Pet Brief

Source patch: 16.9.1
Champion id: Renekton
Display name: Renekton
Pet package id: lol-renekton

## Reference Pack

- Riot official page: https://www.leagueoflegends.com/en-us/champions/renekton/
- Official splash: `references/renekton/ddragon-renekton-splash.jpg`
- Official loading crop: `references/renekton/ddragon-renekton-loading.jpg`
- Model viewer: https://modelviewer.lol/model-viewer?id=58000
- Local model screenshot: `references/renekton/modelviewer-58000.png`
- Notes from visual research: `references/renekton/reference-notes.md`

## Identity

- Core silhouette: compact upright crocodilian Ascended warrior with a long snout, hunched brawler body, thick tail, clawed hands/feet, heavy plated head and shoulders, and an oversized crescent blade held close.
- Palette: teal-green scales, gray stone/steel armor plates, bronze/gold wraps and blade handle, orange eyes, small bright green gem accents.
- Face/personality: furious desert butcher energy; wide crocodile snout, sharp teeth, orange eyes under a heavy brow.
- Must-keep prop or body feature: the crescent blade/polearm, crocodile snout, tail, and heavy head/shoulder armor must stay readable in every row.
- Simplify/remove: remove fine armor cracks, tiny straps, distant enemies, sand scenery, soft glows, loose fury particles, shadows, UI marks, and floating spell icons.

## Ability Mapping

| Ability | Spell name | Codex row | Pet-sized visual cue | Forbidden interpretation |
| --- | --- | --- | --- | --- |
| Q | Cull the Meek | `waving` | one compact circular blade sweep pose with the crescent blade still touching the pet silhouette | Detached slash rings, hit circles, floating blades, enemies, blood, or healing symbols |
| W | Ruthless Predator | `waiting` | crouched snapping stance with both claws and blade held close, jaws clenched as if ready to bite | A separate target, stun icon, shield icon, three floating slash marks, or text |
| E | Slice and Dice | `jumping` | short forward dash/leap body lean with tail and blade tucked close | Speed lines, dust, afterimages, long trails, floor marks, or separate dash arrows |
| R | Dominus | `review` | tyrant stance with broader shoulders, raised head, and a tiny attached hard-edged orange fury accent near the torso | Huge aura, lightning field, enemies, health bar, loose particles, or oversized transformation effects |

## Prompt Notes

- Base pet prompt: A tiny chibi Codex digital pet version of League of Legends Renekton, the Butcher of the Sands: upright crocodile warrior with long green crocodile snout, orange eyes, sharp teeth, teal-green scales, heavy gray stone/steel head and shoulder armor, thick tail, clawed feet, bronze/gold wraps, and an oversized double-ended crescent blade/polearm kept attached to the compact body silhouette. Pixel-art-adjacent flat cel shading, thick dark outline, limited palette, no text, no Riot logo, no scenery.
- Row identity lock: keep the same crocodile snout, orange eyes, teal-green scales, gray armor plates, thick tail, hunched brawler proportions, and crescent blade proportions in every row.
- Chroma-key risk: Renekton uses teal-green scales and bright green gems, so use a flat saturated magenta background and avoid magenta anywhere in the pet.
- Running-left mirror decision: likely safe only if the blade, tail, armor gems, and pose have no side-specific readable mark after `running-right` is generated; inspect before mirroring.

## QA Checklist

- [ ] Reference Pack checked and written into brief.
- [ ] Same silhouette and palette across all rows.
- [ ] Clearly reads as League of Legends Renekton, not a generic dinosaur, dragon, lizard, or human knight.
- [ ] Crocodile snout, orange eyes, heavy armor, tail, and crescent blade remain readable.
- [ ] Q row reads as Cull the Meek without text or detached icons.
- [ ] W row reads as Ruthless Predator without text or detached icons.
- [ ] E row reads as Slice and Dice without text or detached icons.
- [ ] R row reads as Dominus without text or detached icons.
- [ ] Failed row is an app error/reaction state, not confused with Q/W/E/R.
- [ ] Contact sheet has no cropped bodies, white boxes, guide marks, shadows, or loose particles.
- [ ] `qa/review.json` has no errors.
- [ ] `final/validation.json` has no errors.
