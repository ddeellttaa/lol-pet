# Neeko Reference Notes

Source patch: 16.9.1
Champion id: Neeko
Base skin id: 518000

## Sources

- Riot official champion page: https://www.leagueoflegends.com/en-us/champions/neeko/
- Data Dragon splash: `references/neeko/ddragon-neeko-splash.jpg`
- Data Dragon loading crop: `references/neeko/ddragon-neeko-loading.jpg`
- Khada / modelviewer page: https://modelviewer.lol/model-viewer?id=518000

## Visual Observations

- Neeko should read as a small curious chameleon vastaya, not a generic fairy, elf, lizard, or plant mage.
- Main silhouette anchors: large golden eyes, purple-blue hair with magenta edges, two long upward feather/leaf-like hair fins, pink flower on the hair, green arms and legs, orange-brown leaf tunic, dark gloves/feet, and a curled chameleon tail.
- The splash has butterflies, forest light, vines, and glow, but those are scenery cues. They should not become detached pet effects.
- The modelviewer page was reachable from this environment, but no local headless browser was available to capture a reliable WebGL screenshot. The Data Dragon splash and loading crop are therefore the local image references for this run.

## Prompt Risks

- Do not turn Neeko into a generic purple-haired human, fairy, dryad, elf, or small lizard.
- Do not add big loose butterflies, floating flowers, drifting petals, forest scenery, vines crossing cell borders, or glowing spell clouds.
- Avoid magenta, blue, cyan, orange, yellow, red, black, white, gray, and purple chroma-key backgrounds because they overlap generated hair, flower, eyes, clothes, outlines, or shadows. Measured foreground-distance testing on generated Neeko frames found flat saturated green `#00FF00` safest, as her body is muted teal/green rather than pure chroma green.
