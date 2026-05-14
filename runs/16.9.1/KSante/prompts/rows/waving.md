Create a single horizontal sprite strip for the Codex app digital pet `lol-ksante` in the state `waving`.

Use the attached reference image(s) for pet identity and the attached base pet image as the canonical design. Use the attached layout guide image only for frame count, slot spacing, centering, and safe padding. Simplify any high-resolution reference details into the Codex digital pet sprite style. Do not simply copy the still reference pose. Generate distinct animation poses that create a readable cycle.

Identity lock:
- Do not redesign the pet. Only change pose/action for the `waving` animation.
- Preserve the exact head shape, ear/horn/limb shape, face design, markings, palette, outline weight, body proportions, prop design, and overall silhouette from the canonical base pet.
- Keep every frame recognizably the same individual pet, not a related variant.
- If the pet has a prop or accessory, preserve its size, side, palette, and attachment style unless the row action requires a small pose-only adjustment.
- Prefer a subtler animation over any change that mutates the pet identity.

Output exactly 4 separate animation frames arranged left-to-right in one single row. Each frame must show the same pet: # K'Sante Pet Brief

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
- [ ] `final/validation.json` has no errors..

Style contract: Codex digital pet sprite style: pixel-art-adjacent low-resolution mascot sprite, compact chibi proportions, chunky whole-body silhouette, thick dark 1-2 px outline, visible stepped/pixel edges, limited palette, flat cel shading with at most one small highlight and one shadow step, simple readable face, tiny limbs, and no detail that disappears at 192x208. Avoid polished illustration, painterly rendering, anime key art, 3D render, vector app-icon polish, glossy lighting, soft gradients, realistic fur or material texture, anti-aliased high-detail edges, and complex tiny accessories. Additional user style notes: LoL champion fan pet. Compact chibi Codex digital pet; Nazumah warrior identity with paired ntofo weapons; no Riot logo, no text, no detached spell icons..

Use this prompt as an authoritative sprite-production spec. Do not expand it into a polished illustration, painterly character image, anime key art, 3D render, vector mascot, glossy app icon, realistic animal portrait, or marketing artwork.

Animation action: greeting gesture with raised wave and return.


State-specific requirements:
- Show the greeting through paw pose only: paw down, paw raised, paw tilted, paw returning.
- Do not draw wave marks, motion arcs, lines, sparkles, symbols, or floating effects around the paw.

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
- Exactly 4 full-body frames, left to right, in one horizontal row.
- The attached layout guide shows the 4 frame boxes and inner safe area for this row. Follow its slot count, spacing, centering, and padding.
- Do not reproduce the layout guide itself: no visible boxes, guide lines, center marks, labels, guide colors, or guide background may appear in the output.
- Treat the image as 4 equal-width invisible frame slots. Fill every slot: each requested slot must contain exactly one complete full-body pose.
- Spread the 4 poses evenly across the whole image width. Do not leave any requested slot blank or create large empty gaps between poses.
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
