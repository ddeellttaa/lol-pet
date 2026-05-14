Create a single clean reference sprite for a Codex app digital pet named Bard.

Pet: # Bard Pet Brief

Source patch: 16.9.1
Champion id: Bard
Display name: Bard
Pet package id: lol-bard

## Identity

- Core silhouette: compact masked wandering caretaker with a round robed body, little horned hood, broad golden mask-face, tiny feet, and one small bell-chime charm held close.
- Palette: deep teal and violet robe, warm gold mask and trim, muted cream face glow, tiny amber chime accents only when attached to Bard or his charm.
- Face/personality: serene, mysterious, benevolent cosmic guide; sleepy oval mask eyes and calm floating stance.
- Must-keep prop or body feature: the horned hood, gold mask-face, rounded robe body, and small attached chime charm must stay readable in every row.
- Simplify/remove: remove trailing meep swarms, constellations, full portals, large shrine props, complex robe filigree, and loose star fields.

## Ability Mapping

| Ability | Spell name | Codex row | Pet-sized visual cue | Forbidden interpretation |
| --- | --- | --- | --- | --- |
| Q | Cosmic Binding | `waving` | Bard raises the charm/hand forward with one short hard-edged gold tether touching the charm | Long projectile beam, stunned enemies, walls, detached spell icon, or text |
| W | Caretaker's Shrine | `waiting` | Bard cradles a tiny attached shrine-like glow pressed against the robe or feet | Separate floor shrine, healing circle, ally target, loose sparkles, or UI health symbols |
| E | Magical Journey | `jumping` | small arcing hop through a tiny portal rim touching Bard's body | Full terrain portal, tunnel scenery, detached ring, speed lines, or other travelers |
| R | Tempered Fate | `review` | focused stilling pose with Bard's charm lifted and a small attached golden stasis sheen over the mask | Huge golden dome, frozen enemies, map target, halo aura, or cinematic background |

## Prompt Notes

- Base pet prompt: A tiny chibi Codex digital pet version of Bard, the Wandering Caretaker, round robed body, little horned hood, broad golden mask-face with sleepy oval eyes, deep teal and violet robe, warm gold trim, tiny attached bell-chime charm, serene cosmic guide personality, chunky readable silhouette, pixel-art-adjacent flat cel shading, thick dark outline, transparent-friendly solid chroma-key background.
- Row identity lock: keep the same horned hood shape, golden mask-face, rounded robe body, tiny feet, teal-violet-gold palette, and small attached bell-chime charm in every row.
- Chroma-key risk: avoid yellow or orange backgrounds because Bard's mask and chime are gold; use a flat saturated magenta background and keep gold effects opaque, hard-edged, small, and physically attached.
- Running-left mirror decision: likely safe if the charm has no readable markings and the robe lighting is symmetric after `running-right` is generated; inspect before mirroring.

## QA Checklist

- [ ] Same silhouette and palette across all rows.
- [ ] Q row reads as Cosmic Binding without text or detached icons.
- [ ] W row reads as Caretaker's Shrine without text or detached icons.
- [ ] E row reads as Magical Journey without text or detached icons.
- [ ] R row reads as Tempered Fate without text or detached icons.
- [ ] Failed row is an app error/reaction state, not confused with Q/W/E/R.
- [ ] Contact sheet has no cropped bodies, white boxes, guide marks, shadows, or loose particles.
- [ ] `qa/review.json` has no errors.
- [ ] `final/validation.json` has no errors..
Style contract: Codex digital pet sprite style: pixel-art-adjacent low-resolution mascot sprite, compact chibi proportions, chunky whole-body silhouette, thick dark 1-2 px outline, visible stepped/pixel edges, limited palette, flat cel shading with at most one small highlight and one shadow step, simple readable face, tiny limbs, and no detail that disappears at 192x208. Avoid polished illustration, painterly rendering, anime key art, 3D render, vector app-icon polish, glossy lighting, soft gradients, realistic fur or material texture, anti-aliased high-detail edges, and complex tiny accessories. Additional user style notes: LoL champion fan pet. Compact chibi Codex digital pet; wandering cosmic caretaker identity; no Riot logo, no text, no detached spell icons..

Use this prompt as an authoritative sprite-production spec. Do not expand it into a polished illustration, painterly character image, anime key art, 3D render, vector mascot, glossy app icon, realistic animal portrait, or marketing artwork.

Output one centered full-body pet sprite pose only, on a perfectly flat pure user-selected #FF00FF chroma-key background. The pet must be fully visible, readable as a tiny digital pet, and suitable for animation into a 192x208 sprite cell. Do not include scenery, text, labels, borders, checkerboard transparency, detached effects, shadows, glows, or extra props not present in the reference unless explicitly requested. Do not use #FF00FF, pure user-selected, or colors close to that chroma key in the pet, prop, highlights, or effects.
