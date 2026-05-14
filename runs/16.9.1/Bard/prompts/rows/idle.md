Create a single horizontal sprite strip for the Codex app digital pet `lol-bard` in the state `idle`.

Use the attached reference image(s) for pet identity and the attached base pet image as the canonical design. Use the attached layout guide image only for frame count, slot spacing, centering, and safe padding. Simplify any high-resolution reference details into the Codex digital pet sprite style. Do not simply copy the still reference pose. Generate distinct animation poses that create a readable cycle.

Identity lock:
- Do not redesign the pet. Only change pose/action for the `idle` animation.
- Preserve the exact head shape, ear/horn/limb shape, face design, markings, palette, outline weight, body proportions, prop design, and overall silhouette from the canonical base pet.
- Keep every frame recognizably the same individual pet, not a related variant.
- If the pet has a prop or accessory, preserve its size, side, palette, and attachment style unless the row action requires a small pose-only adjustment.
- Prefer a subtler animation over any change that mutates the pet identity.

Output exactly 6 separate animation frames arranged left-to-right in one single row. Each frame must show the same pet: # Bard Pet Brief

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

Animation action: neutral breathing/blinking loop.


Transparency and artifact rules:
- Prefer pose, expression, and silhouette changes over decorative effects.
- Effects are allowed only when they are state-relevant, opaque, hard-edged, pixel-style, fully inside the same frame slot, and physically touching or overlapping the pet silhouette.
- Allowed attached effects can include a tear touching the face, a small smoke puff touching the pet or prop, or tiny stars overlapping the pet during a failed/dizzy reaction.
- Do not draw detached effects: floating stars, loose sparkles, floating punctuation, floating icons, falling tear drops, separated smoke clouds, loose dust, disconnected outline bits, or stray pixels.
- Do not draw wave marks, motion arcs, speed lines, action streaks, afterimages, blur, smears, halos, glows, auras, floor patches, cast shadows, contact shadows, drop shadows, oval floor shadows, landing marks, or impact bursts.
- Do not include text, labels, frame numbers, visible grids, guide marks, speech bubbles, thought bubbles, UI panels, code snippets, scenery, checkerboard transparency, white backgrounds, or black backgrounds.
- Do not use the chroma-key color or chroma-key-adjacent colors in the pet, prop, effects, highlights, shadows, or outlines.
- Reject any pose that is cropped, overlaps another pose, crosses into a neighboring frame slot, or creates a separate disconnected component that is not attached to the pet.

Layout requirements:
- Exactly 6 full-body frames, left to right, in one horizontal row.
- The attached layout guide shows the 6 frame boxes and inner safe area for this row. Follow its slot count, spacing, centering, and padding.
- Do not reproduce the layout guide itself: no visible boxes, guide lines, center marks, labels, guide colors, or guide background may appear in the output.
- Treat the image as 6 equal-width invisible frame slots. Fill every slot: each requested slot must contain exactly one complete full-body pose.
- Spread the 6 poses evenly across the whole image width. Do not leave any requested slot blank or create large empty gaps between poses.
- Center one complete pose in each slot. No pose may cross into the neighboring slot.
- Use a perfectly flat pure user-selected #FF00FF chroma-key background across the whole image.
- Do not draw visible grid lines, borders, labels, numbers, text, watermarks, or checkerboard transparency.
- Do not include scenery or a background environment.
- Keep the rendering sprite-like: chunky silhouette, dark pixel-style outline, limited palette, flat shading, minimal tiny detail.
- Do not use #FF00FF, pure user-selected, or colors close to that chroma key in the pet, props, highlights, shadows, motion marks, dust, landing marks, or effects.
- Do not draw shadows, glows, smears, dust, or landing marks using darker/lighter versions of the chroma-key color.
- Keep every frame self-contained with safe padding. No pet body part should be clipped by the frame slot.
- Avoid motion blur. Use clear pose changes readable at 192x208.
- Preserve the same silhouette, face, proportions, palette, material, and props across every frame.
