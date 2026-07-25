# Datoviz v0.4 Data

This branch stores redistributable, render-ready assets for Datoviz v0.4.

The v0.3 data layout is intentionally not preserved here. Assets are promoted into this branch only
when they are needed by v0.4 examples, fixtures, gallery validation, or reusable runtime resources.

## Layout

```text
examples/          user-facing prepared example bundles
fixtures/          small deterministic validation fixtures
assets/            reusable runtime assets
gallery/baselines/ expected images used by validation
tutorials/          canonical tutorial preview captures
LICENSES/          copied license texts and attribution records
```

Each committed example bundle should include `manifest.json`, `PROVENANCE.md`, and a `prepared/`
directory. Use `BLOCKERS.md` when the intended source cannot be redistributed or regenerated
automatically.

Raw downloads, caches, and scratch conversion outputs belong outside this repository, normally under
the parent repository's `.cache/datoviz/examples/` tree.
