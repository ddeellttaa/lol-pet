Create a single clean reference sprite for a Codex app digital pet named LoL Neeko.

Pet: # Neeko Pet Brief

Source patch: 16.9.1
Champion id: Neeko
Display name: Neeko
Pet package id: lol-neeko

## Reference Pack

- Riot official page: https://www.leagueoflegends.com/en-us/champions/neeko/
- Official splash: `references/neeko/ddragon-neeko-splash.jpg`
- Official loading crop: `references/neeko/ddragon-neeko-loading.jpg`
- Model viewer: https://modelviewer.lol/model-viewer?id=518000
- Local notes: `references/neeko/reference-notes.md`
- Notes from visual research: base Neeko is a curious chameleon vastaya with huge amber eyes, purple-blue hair with magenta tips, two tall leaf/feather hair fins, a pink flower, green limbs, an orange-brown leaf tunic, dark gloves/feet, and a curled chameleon tail. Avoid translating splash scenery, butterflies, and forest glow into detached pet effects.

## Identity

- Core silhouette: compact chibi chameleon-vastaya with oversized golden eyes, big swept purple-blue hair, two tall magenta-tipped leaf/feather hair fins, pink flower on the hair, small green limbs, orange-brown leaf tunic, and a curled tail tucked close.
- Palette: violet-blue hair with magenta tips, warm pink flower, green skin/limbs, orange-brown leaf clothing, dark purple gloves/feet, amber eyes, and only tiny attached green-pink spirit magic.
- Face/personality: bright, curious, playful trickster energy; wide eyes and open delighted expression, but still simplified for 192x208 pet scale.
- Must-keep prop or body feature: the hair fins, flower, amber eyes, green chameleon limbs, leaf tunic, and curled tail must stay readable in every row.
- Simplify/remove: remove forest scenery, butterflies, broad glows, long vines, loose petals, distant clones, detailed jewelry, and tiny body markings that will not read at pet size.

## Ability Mapping

| Ability | Spell name | Codex row | Pet-sized visual cue | Forbidden interpretation |
| --- | --- | --- | --- | --- |
| Q | Blooming Burst | `waving` | Neeko presents one tiny seed or blossom pressed to her hand | Detached flower projectile, repeated explosions, loose petals, butterfly swarm, or spell icon |
| W | Shapesplitter | `waiting` | playful split-stance with a small overlapping same-shape echo attached behind her shoulder | Full second Neeko clone, separate duplicate sprite, afterimage trail, mirror text, or detached silhouette |
| E | Tangle-Barbs | `jumping` | short hop while holding a tiny vine/barb coil touching her hands or tail | Long snare line across cells, rooted enemy, ground vines, thorn field, or loose plant particles |
| R | Pop Blossom | `review` | focused crouch-to-blossom pose with a small flower-burst collar attached around her body | Huge flower explosion, airborne enemies, wide aura, falling petals, halo, or cinematic background |

## Prompt Notes

- Base pet prompt: A tiny chibi Codex digital pet version of League of Legends Neeko, curious chameleon vastaya, huge amber-gold eyes, big swept purple-blue hair with magenta tips, two tall leaf-like magenta hair fins, pink flower in the hair, green arms and legs, orange-brown leaf tunic, dark purple glove hands and feet, curled chameleon tail tucked close, playful open expression, compact readable whole-body silhouette, pixel-art-adjacent flat cel shading, thick dark outline, transparent-friendly solid chroma-key background.
- Row identity lock: keep the same huge amber eyes, purple-blue and magenta hair shape, two tall hair fins, pink flower, green limbs, orange-brown leaf tunic, dark gloves/feet, curled tail, curious expression, and compact chameleon-vastaya silhouette in every row.
- Chroma-key risk: measured generated Neeko foreground colors are safest against flat saturated green `#00FF00`; keep the body green muted/teal rather than pure chroma green, and keep all highlights away from the key color.
- Running-left mirror decision: likely safe only if the flower, hair fins, tail curl, and leaf tunic still read naturally after `running-right`; inspect before mirroring because the flower and tail may make left-right asymmetry noticeable.

## QA Checklist

- [ ] Reference Pack 已查并写入 brief。
- [ ] Same silhouette and palette across all rows.
- [ ] Reads as League of Legends Neeko, not a generic fairy, elf, dryad, or lizard.
- [ ] Hair fins, pink flower, amber eyes, green limbs, leaf tunic, and curled tail stay readable.
- [ ] Q row reads as Blooming Burst without text or detached icons.
- [ ] W row reads as Shapesplitter without a separate full clone sprite.
- [ ] E row reads as Tangle-Barbs without long detached vine lines.
- [ ] R row reads as Pop Blossom without huge detached flower explosions.
- [ ] Failed row is an app error/reaction state, not confused with Q/W/E/R.
- [ ] Contact sheet has no cropped bodies, white boxes, guide marks, shadows, or loose particles.
- [ ] `qa/review.json` has no errors.
- [ ] `final/validation.json` has no errors..
Style contract: Codex digital pet sprite style: pixel-art-adjacent low-resolution mascot sprite, compact chibi proportions, chunky whole-body silhouette, thick dark 1-2 px outline, visible stepped/pixel edges, limited palette, flat cel shading with at most one small highlight and one shadow step, simple readable face, tiny limbs, and no detail that disappears at 192x208. Avoid polished illustration, painterly rendering, anime key art, 3D render, vector app-icon polish, glossy lighting, soft gradients, realistic fur or material texture, anti-aliased high-detail edges, and complex tiny accessories. Additional user style notes: LoL champion fan pet. Compact chibi Codex digital pet; curious chameleon vastaya identity; no Riot logo, no text, no detached spell icons..

Use this prompt as an authoritative sprite-production spec. Do not expand it into a polished illustration, painterly character image, anime key art, 3D render, vector mascot, glossy app icon, realistic animal portrait, or marketing artwork.

Output one centered full-body pet sprite pose only, on a perfectly flat pure user-selected #00FF00 chroma-key background. The pet must be fully visible, readable as a tiny digital pet, and suitable for animation into a 192x208 sprite cell. Do not include scenery, text, labels, borders, checkerboard transparency, detached effects, shadows, glows, or extra props not present in the reference unless explicitly requested. Do not use #00FF00, pure user-selected, or colors close to that chroma key in the pet, prop, highlights, or effects.
