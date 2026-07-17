# McHenrys Peak Terrain Relief

## Source

- Bare-earth elevation: USGS 3D Elevation Program dynamic image service.
- Natural-color texture: USGS The National Map NAIP Plus image service.
- WGS84 crop: (-105.705, 40.245, -105.625, 40.31) around McHenrys Peak and Glacier Gorge, Colorado.

## Processing

- Both rasters were exported into EPSG:26913 over the same projected extent.
- Elevation was sampled to 490x512 float32 meters.
- Imagery was sampled to 1960x2048 RGB pixels.
- The imagery received restrained autocontrast, saturation, contrast, and brightness grading.

## License And Attribution

- USGS 3DEP products are public domain and available without use restrictions.
- NAIP imagery acquired by USDA has been placed in the public domain.
- Credit: U.S. Geological Survey 3DEP and USDA National Agriculture Imagery Program.

## Notes

- The ArcGIS service descriptions and exact export requests are retained under source/.
- Service-backed source mosaics evolve; the manifest records checksums for this prepared snapshot.
