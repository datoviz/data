# Catalogued Orbital Debris

## Source

- CelesTrak OMM-compatible GP element sets for FENGYUN 1C, IRIDIUM 33, and COSMOS 2251 debris.
- Snapshot retrieval time: 2026-07-16T11:29:20Z.
- CelesTrak GP documentation: https://celestrak.org/NORAD/documentation/gp-data-formats.php

## Processing

- Propagated each accepted GP element set with python-sgp4 2.25.
- Converted TEME positions to approximate Earth-fixed coordinates using GMST and normalized by 6378.137 km.
- Generated 121 frames for 2508 catalogued objects at 60-second intervals.
- Generated one closed 121-sample inertial trajectory per object.

## License And Attribution

- CelesTrak data is freely provided subject to its usage policy: https://celestrak.org/usage-policy.php
- SGP4 implementation follows Vallado et al.; cite https://celestrak.org/publications/AIAA/2006-6753/

## Notes

- These are tracked catalog objects from three selected debris events, not the full debris environment.
- The Earth-fixed conversion omits polar motion and other high-precision Earth-orientation corrections.
- Point sizes in the visualization are exaggerated and do not encode physical object size.
