# RESEPI RGB LiDAR Point Cloud Browser Bundle

## Source And Attribution

- Source: Inertial Labs RESEPI sample data, `RESEPI-GENM2X-COLORIZED-50M-10MS-STRIP-OUTLIER.laz`.
- Sample page: <https://lidarpayload.com/sample-data/>.
- Public viewer: <https://app.stitch3d.io/viewer/689bab260195cc818197583b>.
- Raw source SHA-256: `08d4c50d15efa496c8c5f8168a4331260fe85797f7412506aea5a1c1885add45`.
- Redistribution permission received; permission details pending.

The raw LAZ source is not included in this bundle. Replace the provisional permission statement with the grantor, date, scope, and durable reference when those details are available.

## Processing

Run `python3 tools/data/prepare_point_cloud.py --force` from the Datoviz repository root to prepare the six-million-point native cache and deterministic browser subset. The browser artifact selects 500,000 linearly spaced records from the prepared native bundle and retains normalized XYZ positions, direct RGBA colors, and per-point pixel sizes.

## Published File

- `prepared/point_cloud.bin`: 500,000 little-endian v2 point records plus the `DVZPCD1` header, 16,000,040 bytes, SHA-256 `ad5b997813ca275a9eb47b4250bb0acebc9a8a8df42fb250c1e199ec9c97d797`.
