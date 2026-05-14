# Bard Pet Brief

Source patch: 16.9.1
Champion id: Bard
Display name: Bard
Pet package id: lol-bard

## Identity

- Core silhouette: compact rotund chibi version of League of Legends Bard, the Wandering Caretaker, based on official splash/loading art: huge flowing cream-white beard/mane, small ochre-gold glowing face plate/face area with three luminous spots, red/burgundy torso cloth, oversized dark mittens, bulky curled legs, and small meeps.
- Palette: deep burgundy/red cloth, charcoal-dark gloves/legs, warm ochre-gold face glow and meeps, cream-white beard, muted brown/stone body surfaces, and tiny gold trim only when attached to Bard or a meep.
- Face/personality: serene, ancient, mysterious, benevolent cosmic caretaker; face reads as Bard's small glowing face area, not a human face, robot helmet, knight mask, or cute santa face.
- Must-keep feature: the three-light ochre face, huge white beard/mane, burgundy torso, dark oversized mittens, bulky rounded body, and small meep identity cues must stay readable in every row.
- Must-remove from earlier wrong versions: no wizard hat, no hooded robe silhouette, no horned hood, no dangling bells or chimes added as accessories, no Santa/dwarf face, no visible human mouth, no teal cloak redesign.

## Ability Mapping

| Ability | Spell name | Codex row | Pet-sized visual cue | Forbidden interpretation |
| --- | --- | --- | --- | --- |
| Q | Cosmic Binding | `waving` | Bard raises one dark mitten/hand forward with a tiny attached gold spark touching the hand | Long projectile beam, stunned enemies, walls, detached spell icon, or text |
| W | Caretaker's Shrine | `waiting` | Bard calmly holds a tiny attached warm glow against his body | Separate floor shrine, healing circle, ally target, loose sparkles, bells, chimes, or UI health symbols |
| E | Magical Journey | `jumping` | Bard makes a small hop; if a portal cue appears, it must be a tiny rim touching the body | Full terrain portal, tunnel scenery, detached ring, speed lines, or other travelers |
| R | Tempered Fate | `review` | focused stilling pose with a subtle attached golden sheen near the face | Huge golden dome, frozen enemies, map target, halo aura, or cinematic background |

## Prompt Notes

- Base pet prompt: A tiny chibi Codex digital pet version of League of Legends Bard, the Wandering Caretaker, based on official Bard splash/loading/model references: small ochre-gold glowing Bard face area with three luminous dots, enormous cream-white beard and mane surrounding and hanging below the face, round squat burgundy/red torso cloth, dark oversized mitten hands, chunky curled legs/feet, muted brown/stone body surfaces, and one or two tiny meep-like golden spirits touching the side. No wizard hat, no hood, no horns, no dangling bells, no chime accessories, no human mouth, no santa/dwarf face, no teal cloak.
- Row identity lock: keep the same three-light ochre face, huge white beard/mane, round burgundy body, dark mittens, chunky legs, and attached meep cue in every row.
- Chroma-key risk: avoid yellow/orange backgrounds because Bard's face and meeps are warm gold; use a flat saturated magenta background and keep all gold effects opaque, hard-edged, small, and physically attached.
- Running-left mirror decision: likely safe only if the meep cue, face lights, and body silhouette remain semantically correct after `running-right`; inspect before mirroring.

## Reference Pack

- Official champion page: https://www.leagueoflegends.com/en-us/champions/bard/
- Official splash: `references/bard/ddragon-bard-splash.jpg`
- Official loading crop: `references/bard/ddragon-bard-loading.jpg`
- Khada 3D model page: https://modelviewer.lol/model-viewer?id=432000
- Khada model resource id: `lol/models/bard/432000`
- Khada circle crop: `references/bard/khada-bard-circle-432000.webp`

## QA Checklist

- [ ] Same silhouette and palette across all rows.
- [ ] Clearly reads as League of Legends Bard, not a generic wizard/idol/santa/dwarf.
- [ ] No wizard hat, hood, horns, dangling bells, or dangling chimes.
- [ ] Face reads as Bard's three-light ochre face area, not a human face or robot helmet.
- [ ] Huge white beard/mane and burgundy body remain dominant.
- [ ] Small meep cue stays physically attached when present.
- [ ] Q row reads as Cosmic Binding without text or detached icons.
- [ ] W row reads as Caretaker's Shrine without text or detached icons.
- [ ] E row reads as Magical Journey without text or detached icons.
- [ ] R row reads as Tempered Fate without text or detached icons.
- [ ] Contact sheet has no cropped bodies, white boxes, guide marks, shadows, or loose particles.
- [ ] `qa/review.json` has no errors.
- [ ] `final/validation.json` has no errors.
