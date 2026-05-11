Create a single horizontal sprite strip for the Codex app digital pet `lol-aatrox` in the state `jumping`.

Use the attached reference image(s) for pet identity and the attached base pet image as the canonical design. Use the attached layout guide image only for frame count, slot spacing, centering, and safe padding. Simplify any high-resolution reference details into the Codex digital pet sprite style. Do not simply copy the still reference pose. Generate distinct animation poses that create a readable cycle.

Identity lock:
- Do not redesign the pet. Only change pose/action for the `jumping` animation.
- Preserve the exact head shape, ear/horn/limb shape, face design, markings, palette, outline weight, body proportions, prop design, and overall silhouette from the canonical base pet.
- Keep every frame recognizably the same individual pet, not a related variant.
- If the pet has a prop or accessory, preserve its size, side, palette, and attachment style unless the row action requires a small pose-only adjustment.
- Prefer a subtler animation over any change that mutates the pet identity.

Output exactly 5 separate animation frames arranged left-to-right in one single row. Each frame must show the same pet: # Aatrox Pet Brief

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

Animation action: anticipation, lift, peak, descent, settle.


State-specific requirements:
- Show the jump through pose and vertical body position only: anticipation, lift, airborne peak, descent, settle.
- Do not draw ground shadows, contact shadows, drop shadows, oval shadows, landing marks, dust, smears, bounce pads, or motion marks under the pet.
- Keep the background outside the pet perfectly flat chroma key with no darker key-colored patches.

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
- Exactly 5 full-body frames, left to right, in one horizontal row.
- The attached layout guide shows the 5 frame boxes and inner safe area for this row. Follow its slot count, spacing, centering, and padding.
- Do not reproduce the layout guide itself: no visible boxes, guide lines, center marks, labels, guide colors, or guide background may appear in the output.
- Treat the image as 5 equal-width invisible frame slots. Fill every slot: each requested slot must contain exactly one complete full-body pose.
- Spread the 5 poses evenly across the whole image width. Do not leave any requested slot blank or create large empty gaps between poses.
- Center one complete pose in each slot. No pose may cross into the neighboring slot.
- Use a perfectly flat pure user-selected #00FF00 chroma-key background across the whole image.
- Do not draw visible grid lines, borders, labels, numbers, text, watermarks, or checkerboard transparency.
- Do not include scenery or a background environment.
- Keep the rendering sprite-like: chunky silhouette, dark pixel-style outline, limited palette, flat shading, minimal tiny detail.
- Do not use #00FF00, pure user-selected, or colors close to that chroma key in the pet, props, highlights, shadows, motion marks, dust, landing marks, or effects.
- Do not draw shadows, glows, smears, dust, or landing marks using darker/lighter versions of the chroma-key color.
- Keep every frame self-contained with safe padding. No pet body part should be clipped by the frame slot.
- Avoid motion blur. Use clear pose changes readable at 192x208.
- Preserve the same silhouette, face, proportions, palette, material, and props across every frame.
