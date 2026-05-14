# Aphelios Pet Brief

Source patch: 16.9.1
Champion id: Aphelios
Display name: Aphelios
Pet package id: lol-aphelios

## Identity

- Core silhouette: compact silent Lunari marksman with side-swept dark hair, pale face, dark fitted coat, purple shoulder mantle, moon-silver armor plates, and one crescent-shaped gun/blade held close.
- Palette: deep black/navy clothing, muted violet mantle, moon-silver metal, pale cyan-blue glow used sparingly, tiny magenta-pink energy only when attached to the weapon.
- Face/personality: brooding, quiet, focused, almost ceremonial; small narrowed eyes and a composed stance.
- Must-keep prop or body feature: the crescent weapon silhouette, purple mantle, side-swept hair, and moon-silver Lunari palette must stay readable in every row.
- Simplify/remove: do not show all five weapons at once, Alune as a separate character, floating moon sigils, long laser beams, large cone blasts, sentries, ammo UI, weapon queue UI, or detailed splash-art armor filigree.

## Ability Mapping

| Ability | Spell name | Codex row | Pet-sized visual cue | Forbidden interpretation |
| --- | --- | --- | --- | --- |
| Q | Weapon Abilities | `waving` | a compact raised crescent gun/blade pose with a tiny attached moonshot spark on the weapon | Five separate weapons, detached bullet trails, target marks, turret/sentry, enemy target, or skill icon |
| W | Phase | `waiting` | calm two-weapon swap stance, one crescent weapon tucked in and one tiny off-hand barrel hinted close to the body | UI swap arrows, floating weapon wheel, text labels, inventory icons, or a separate Alune figure |
| E | Weapon Queue System | `jumping` | small upward readiness hop with a tiny next-weapon crescent tucked behind the shoulder | HUD queue, numbered ammo, floating weapon order, detached moon icons, or explanatory symbols |
| R | Moonlight Vigil | `review` | focused kneeling or aiming stance with one short attached moonlight glow at the crescent weapon | Giant lunar beam, area explosion, raining attacks, enemy champion, full moon backdrop, or detached aura |

## Prompt Notes

- Base pet prompt: A tiny chibi Codex digital pet version of Aphelios, silent Lunari marksman, side-swept dark hair, pale focused face, dark navy-black outfit, muted violet shoulder mantle, moon-silver armor accents, compact crescent-shaped moon gun/blade held close, small cyan-blue Lunari glow, brooding ceremonial posture, chunky readable silhouette, pixel-art-adjacent flat cel shading, thick dark outline, transparent-friendly solid chroma-key background.
- Row identity lock: keep the same side-swept hair, pale face, violet mantle, dark coat, moon-silver crescent weapon, compact marksman posture, and restrained cyan/magenta weapon glow in every row.
- Chroma-key risk: avoid blue/cyan chroma backgrounds because Aphelios uses moon-blue glow; use a flat saturated green background and keep glow opaque, tiny, hard-edged, and attached to the weapon or body.
- Running-left mirror decision: likely risky because the crescent weapon and hair/mantle silhouette are asymmetric; inspect `running-right` before mirroring, and prefer a separately generated left run if the crescent flips awkwardly.

## QA Checklist

- [x] Same silhouette and palette across all rows.
- [x] Q row reads as Weapon Abilities without text, UI, detached bullets, or five-weapon clutter.
- [x] W row reads as Phase without arrows, labels, or a weapon-wheel UI.
- [x] E row reads as Weapon Queue System without HUD, numbers, or floating icons.
- [x] R row reads as Moonlight Vigil without a giant beam, explosion, enemy, or moon backdrop.
- [x] Failed row is an app error/reaction state, not confused with Q/W/E/R.
- [x] Contact sheet has no cropped bodies, white boxes, guide marks, shadows, or loose particles.
- [x] `qa/review.json` has no errors.
- [x] `final/validation.json` has no errors.
