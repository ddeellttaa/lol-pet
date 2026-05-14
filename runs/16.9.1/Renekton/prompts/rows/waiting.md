Create a single horizontal sprite strip for the Codex app digital pet `lol-renekton` in the state `waiting`.

Use the attached reference image(s) for pet identity and the attached base pet image as the canonical design. Use the attached layout guide image only for frame count, slot spacing, centering, and safe padding. Simplify any high-resolution reference details into the Codex digital pet sprite style. Do not simply copy the still reference pose. Generate distinct animation poses that create a readable cycle.

Identity lock:
- Do not redesign the pet. Only change pose/action for the `waiting` animation.
- Preserve the exact head shape, ear/horn/limb shape, face design, markings, palette, outline weight, body proportions, prop design, and overall silhouette from the canonical base pet.
- Keep every frame recognizably the same individual pet, not a related variant.
- If the pet has a prop or accessory, preserve its size, side, palette, and attachment style unless the row action requires a small pose-only adjustment.
- Prefer a subtler animation over any change that mutates the pet identity.

Output exactly 6 separate animation frames arranged left-to-right in one single row. Each frame must show the same pet: # Renekton Pet Brief

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
- [ ] `final/validation.json` has no errors..

Style contract: Codex digital pet sprite style: pixel-art-adjacent low-resolution mascot sprite, compact chibi proportions, chunky whole-body silhouette, thick dark 1-2 px outline, visible stepped/pixel edges, limited palette, flat cel shading with at most one small highlight and one shadow step, simple readable face, tiny limbs, and no detail that disappears at 192x208. Avoid polished illustration, painterly rendering, anime key art, 3D render, vector app-icon polish, glossy lighting, soft gradients, realistic fur or material texture, anti-aliased high-detail edges, and complex tiny accessories. Additional user style notes: LoL champion fan pet. Compact chibi Codex digital pet; Renekton crocodilian Ascended warrior identity; no Riot logo, no text, no detached spell icons..

Use this prompt as an authoritative sprite-production spec. Do not expand it into a polished illustration, painterly character image, anime key art, 3D render, vector mascot, glossy app icon, realistic animal portrait, or marketing artwork.

Animation action: patient waiting loop with small motion.


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
