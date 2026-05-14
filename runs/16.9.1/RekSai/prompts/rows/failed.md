Create a single horizontal sprite strip for the Codex app digital pet `lol-reksai` in the state `failed`.

Use the attached reference image(s) for pet identity and the attached base pet image as the canonical design. Use the attached layout guide image only for frame count, slot spacing, centering, and safe padding. Simplify any high-resolution reference details into the Codex digital pet sprite style. Do not simply copy the still reference pose. Generate distinct animation poses that create a readable cycle.

Identity lock:
- Do not redesign the pet. Only change pose/action for the `failed` animation.
- Preserve the exact head shape, ear/horn/limb shape, face design, markings, palette, outline weight, body proportions, prop design, and overall silhouette from the canonical base pet.
- Keep every frame recognizably the same individual pet, not a related variant.
- If the pet has a prop or accessory, preserve its size, side, palette, and attachment style unless the row action requires a small pose-only adjustment.
- Prefer a subtler animation over any change that mutates the pet identity.

Output exactly 8 separate animation frames arranged left-to-right in one single row. Each frame must show the same pet: # Rek'Sai Pet Brief

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
- [ ] `final/validation.json` has no errors..

Style contract: Codex digital pet sprite style: pixel-art-adjacent low-resolution mascot sprite, compact chibi proportions, chunky whole-body silhouette, thick dark 1-2 px outline, visible stepped/pixel edges, limited palette, flat cel shading with at most one small highlight and one shadow step, simple readable face, tiny limbs, and no detail that disappears at 192x208. Avoid polished illustration, painterly rendering, anime key art, 3D render, vector app-icon polish, glossy lighting, soft gradients, realistic fur or material texture, anti-aliased high-detail edges, and complex tiny accessories. Additional user style notes: LoL champion fan pet. Compact chibi Codex digital pet; Rek'Sai quadrupedal Void predator identity; no Riot logo, no text, no detached spell icons..

Use this prompt as an authoritative sprite-production spec. Do not expand it into a polished illustration, painterly character image, anime key art, 3D render, vector mascot, glossy app icon, realistic animal portrait, or marketing artwork.

Animation action: sad, failed, or deflated reaction.


State-specific requirements:
- Show failure through slumped pose, drooping ears/limbs, closed or sad eyes, and lower body position.
- Tears, small smoke puffs, or tiny stars are allowed only if attached to or overlapping the pet silhouette and kept inside the same frame slot.
- Do not draw red X marks, floating symbols, detached stars, separated smoke clouds, falling tear drops, dust, or other loose effects.

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
- Exactly 8 full-body frames, left to right, in one horizontal row.
- The attached layout guide shows the 8 frame boxes and inner safe area for this row. Follow its slot count, spacing, centering, and padding.
- Do not reproduce the layout guide itself: no visible boxes, guide lines, center marks, labels, guide colors, or guide background may appear in the output.
- Treat the image as 8 equal-width invisible frame slots. Fill every slot: each requested slot must contain exactly one complete full-body pose.
- Spread the 8 poses evenly across the whole image width. Do not leave any requested slot blank or create large empty gaps between poses.
- Center one complete pose in each slot. No pose may cross into the neighboring slot.
- Use a perfectly flat pure green #00FF00 chroma-key background across the whole image.
- Do not draw visible grid lines, borders, labels, numbers, text, watermarks, or checkerboard transparency.
- Do not include scenery or a background environment.
- Keep the rendering sprite-like: chunky silhouette, dark pixel-style outline, limited palette, flat shading, minimal tiny detail.
- Do not use #00FF00, pure green, or colors close to that chroma key in the pet, props, highlights, shadows, motion marks, dust, landing marks, or effects.
- Do not draw shadows, glows, smears, dust, or landing marks using darker/lighter versions of the chroma-key color.
- Keep every frame self-contained with safe padding. No pet body part should be clipped by the frame slot.
- Avoid motion blur. Use clear pose changes readable at 192x208.
- Preserve the same silhouette, face, proportions, palette, material, and props across every frame.
