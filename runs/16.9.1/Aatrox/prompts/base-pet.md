Create a single clean reference sprite for a Codex app digital pet named LoL Aatrox.

Pet: # Aatrox Pet Brief

Source patch: 16.9.1
Champion id: Aatrox
Display name: Aatrox
Pet package id: lol-aatrox

## Identity

- Core silhouette: compact darkin swordsman with horned head, small wing-like back points, oversized crimson greatsword.
- Palette: blackened armor, deep red flesh/accents, bone-white blade edge highlights, very small gold/brass armor notes.
- Face/personality: stern, furious, ancient warlord energy; small glowing eyes under a heavy brow.
- Must-keep prop or body feature: the massive darkin greatsword must stay attached to the body silhouette in every row.
- Simplify/remove: remove fine armor filigree, splash-art chains, large wings, distant enemies, ground decals, soft glows, and loose blood/energy particles.

## Ability Mapping

| Ability | Spell name | Codex row | Pet-sized visual cue | Forbidden interpretation |
| --- | --- | --- | --- | --- |
| Q | The Darkin Blade | `waving` | one compact overhead greatsword wind-up/slam pose, blade still touching the pet silhouette | Three separate hit zones, floating slash arcs, impact marks, or ground cracks |
| W | Infernal Chains | `waiting` | crouched bracing stance with one short hard-edged chain wrapped close around the sword or forearm | Detached chain projectile, target reticle, impact circle, or dragged enemy |
| E | Umbral Dash | `jumping` | short forward dash body lean with sword tucked close and feet lifted | Speed lines, afterimages, dust, floor shadow, or long motion trail |
| R | World Ender | `review` | tiny demonic stance with slightly larger horns/back points and raised sword | Full-size wings, aura halo, fear icons, minions, or broad red glow |

## Prompt Notes

- Base pet prompt: A tiny chibi Codex digital pet version of Aatrox, dark red and black armored darkin swordsman, horned head, small wing-like back points, oversized crimson greatsword, chunky readable silhouette, pixel-art-adjacent flat cel shading, thick dark outline, transparent-friendly solid chroma-key background.
- Row identity lock: keep the same horn shape, glowing eyes, red-black palette, compact armor mass, and oversized greatsword proportions in every row.
- Chroma-key risk: avoid green accents; use a flat saturated green background and keep all red effects opaque, hard-edged, and attached to the pet.
- Running-left mirror decision: likely safe only if the greatsword has no asymmetric markings or side-specific pose after `running-right` is generated; inspect before mirroring.

## QA Checklist

- [ ] Same silhouette and palette across all rows.
- [ ] Q row reads as The Darkin Blade without text or detached icons.
- [ ] W row reads as Infernal Chains without text or detached icons.
- [ ] E row reads as Umbral Dash without text or detached icons.
- [ ] R row reads as World Ender without text or detached icons.
- [ ] Failed row is an app error/reaction state, not confused with Q/W/E/R.
- [ ] Contact sheet has no cropped bodies, white boxes, guide marks, shadows, or loose particles.
- [ ] `qa/review.json` has no errors.
- [ ] `final/validation.json` has no errors..
Style contract: Codex digital pet sprite style: pixel-art-adjacent low-resolution mascot sprite, compact chibi proportions, chunky whole-body silhouette, thick dark 1-2 px outline, visible stepped/pixel edges, limited palette, flat cel shading with at most one small highlight and one shadow step, simple readable face, tiny limbs, and no detail that disappears at 192x208. Avoid polished illustration, painterly rendering, anime key art, 3D render, vector app-icon polish, glossy lighting, soft gradients, realistic fur or material texture, anti-aliased high-detail edges, and complex tiny accessories. Additional user style notes: LoL champion fan pet. Compact chibi Codex digital pet; darkin swordsman identity; no Riot logo, no text, no detached spell icons..

Use this prompt as an authoritative sprite-production spec. Do not expand it into a polished illustration, painterly character image, anime key art, 3D render, vector mascot, glossy app icon, realistic animal portrait, or marketing artwork.

Output one centered full-body pet sprite pose only, on a perfectly flat pure user-selected #00FF00 chroma-key background. The pet must be fully visible, readable as a tiny digital pet, and suitable for animation into a 192x208 sprite cell. Do not include scenery, text, labels, borders, checkerboard transparency, detached effects, shadows, glows, or extra props not present in the reference unless explicitly requested. Do not use #00FF00, pure user-selected, or colors close to that chroma key in the pet, prop, highlights, or effects.
