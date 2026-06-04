# Runtime Asset Provenance

These assets were promoted from the historical Datoviz data repository commit
`0533e009304effd2af11417a4177ef0276909a2f` into the v0.4 layout.

## Fonts

- `fonts/Roboto-*.ttf`: Roboto family files used by the scene text fallback path.
- `fonts/RobotoMono-Medium.ttf`: Roboto Mono fallback used by monospaced text requests.
- `fonts/Inconsolata-Regular.ttf`: Inconsolata fallback used by text examples and diagnostics.
- `fonts/DroidSans.ttf`: Droid Sans fallback retained for existing text-family lookup behavior.

Before final public packaging, replace this inherited record with copied license texts or exact source
links in `LICENSES/`.

## Textures

- `textures/world.200412.3x5400x2700.jpg`: Earth texture used by textured mesh and planet examples.
- `textures/earth.jpg`: compact Earth fallback texture.
- `textures/mars_viking_mdim21.jpg`: Mars texture used by the planet showcase.

Before final public packaging, record source URLs, license terms, and attribution requirements in
`LICENSES/`.

## Colormaps

- `colormaps/cmap_atlas.csv`
- `colormaps/cmap_atlas.img`
- `colormaps/cmap_atlas.png`

These files are retained as reusable runtime colormap resources. Keep generated replacements
script-backed when the colormap pipeline is refreshed.
