# Yasuo Pet Brief

Source patch: 16.9.1
Champion id: Yasuo
Display name: Yasuo
Pet package id: lol-yasuo

## Identity

- Core silhouette: compact wandering swordsman with high swept hair, long scarf/sash, shoulder guard, and a katana held close to the body.
- Palette: muted navy cloth, steel-gray armor, tan skin, dark hair, small teal wind accents only when attached to sword or body.
- Face/personality: focused, stubborn, wind-worn ronin energy; narrowed eyes and calm stance.
- Must-keep prop or body feature: the katana and swept hair/scarf silhouette must stay readable in every row.
- Simplify/remove: remove fine armor lacing, face scars too small to read, broad wind tornadoes, loose petals, distant enemies, and large transparent gust effects.

## Ability Mapping

| Ability | Spell name | Codex row | Pet-sized visual cue | Forbidden interpretation |
| --- | --- | --- | --- | --- |
| Q | Steel Tempest | `waving` | compact forward katana thrust or raised slash pose, with any wind cue touching the blade | Detached whirlwind, long slash arc, airborne target, impact marks, or skill icon |
| W | Wind Wall | `waiting` | braced stance with one short hard-edged wind shield pressed against the sword or forearm | Full wall panel, rectangular barrier, loose gust bands, projectiles, or scenery |
| E | Sweeping Blade | `jumping` | short dash-like lift with body leaning through the katana line | Speed lines, afterimages, dust, target enemy, or floor shadow |
| R | Last Breath | `review` | focused airborne finishing stance with katana raised close and scarf lifted | Enemy suspended nearby, huge cyclone, aura halo, text, or cinematic background |

## Prompt Notes

- Base pet prompt: A tiny chibi Codex digital pet version of Yasuo, wandering ronin swordsman, high swept dark hair, small shoulder guard, long scarf/sash, compact katana, muted navy cloth and steel armor, stubborn focused face, chunky readable silhouette, pixel-art-adjacent flat cel shading, thick dark outline, transparent-friendly solid chroma-key background.
- Row identity lock: keep the same swept hair shape, scarf/sash, katana length, shoulder guard, muted navy-and-steel palette, and compact ronin silhouette in every row.
- Chroma-key risk: avoid cyan/teal backgrounds because small wind accents may use teal; use a flat saturated magenta background and keep wind cues opaque, hard-edged, small, and attached to Yasuo or the katana.
- Running-left mirror decision: likely safe if the katana and scarf have no readable markings or side-specific lighting after `running-right` is generated; inspect before mirroring.

## QA Checklist

- [x] Same silhouette and palette across all rows.
- [x] Q row reads as Steel Tempest without text or detached icons.
- [x] W row reads as Wind Wall without text or detached icons.
- [x] E row reads as Sweeping Blade without text or detached icons.
- [x] R row reads as Last Breath without text or detached icons.
- [x] Failed row is an app error/reaction state, not confused with Q/W/E/R.
- [x] Contact sheet has no cropped bodies, white boxes, guide marks, shadows, or loose particles.
- [x] `qa/review.json` has no errors.
- [x] `final/validation.json` has no errors.
