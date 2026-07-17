# SVG Tiger Prepared Paths

## Source And Attribution

- The artwork comes from Nicolas P. Rougier's Glumpy example gallery.
- Upstream gallery: <https://glumpy.github.io/gallery.html>
- Pinned source: `glumpy/data/tiger.svg` at Glumpy commit
  `aedb9212a1e00a68b7c4669405a6a8f754daf283`.
- Pinned source SHA-256:
  `1bc237707ae0523f0e2115917626bfaceb24bc4a388b5ef659b5604b311ff537`.
- Citation: Nicolas P. Rougier, Glumpy example gallery, classic SVG Tiger example.

The Datoviz maintainer confirmed redistribution of this pinned artwork and its prepared derivative
for this release. The upstream SVG itself is not included in this bundle.

## Processing

Run from the Datoviz repository root:

```sh
python3 tools/data/prepare_svg_tiger.py --download
```

The preparation tool verifies the pinned source byte count and SHA-256, resolves Glumpy-compatible
inherited paint, flattens `M`, `L`, `C`, and `Z` paths with adaptive De Casteljau subdivision, and
writes deterministic path records plus float64 points. Datoviz triangulates fills with Earcut and
renders outlines as retained paths.

## Published Files

- `prepared/tiger_paths.bin`: deterministic prepared path bundle used by native and WebGPU routes.
- `prepared/metadata.json`: source, processing, document-shape, and artifact-hash metadata.
