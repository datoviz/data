# Vulkan Tutorial Preview Provenance

These canonical previews were rendered from Datoviz commit `1a748def30e8f4bf35f3630df4283cff78dfbd6c` on macOS through MoltenVK.

Each executable ran with `--offscreen --frames 3 --validate --png <path>`. The captures are `800x600` non-interlaced RGBA PNGs and passed the Datoviz nonblank-image validator without Vulkan validation errors.

| File | Executable | SHA-256 |
| --- | --- | --- |
| `first-triangle.png` | `first_triangle` | `6ad0ec41c833bbc846fc32a109627bfa25520e17fa1d690addb265e70c1813d0` |
| `shaders-and-pipeline.png` | `shaders_and_pipeline` | `5f90920d54be11cda8f1e0107c6ae09152520512c622ff4064b071af1ed30a04` |
| `vertex-buffers.png` | `vertex_buffers` | `6ad0ec41c833bbc846fc32a109627bfa25520e17fa1d690addb265e70c1813d0` |

The first and third captures are intentionally identical: chapter three changes the vertex-data source from shader constants to an explicit GPU buffer while preserving the rendered result.

These project-generated images are distributed under the Datoviz MIT license.
