# Human Auditory Cortical Activity

## Source

- OpenNeuro `ds000248` snapshot `1.2.4` (10.18112/openneuro.ds000248.v1.2.4).
- Participant `sub-01`; simultaneous audiovisual MEG/EEG experiment; this derivative uses MEG only.
- Every downloaded source file is checked against a pinned byte count and MD5 or SHA-256 digest.

## Processing

- Filtered MEG channels from 1 to 40 Hz.
- Epoched `Auditory/Left` trials from -0.2 to 0.5 seconds and baseline-corrected through stimulus onset.
- Estimated baseline noise covariance, participant-native BEM/forward solution, and a loose-orientation minimum-norm inverse.
- Applied dSPM with SNR=3 and lambda2=0.111111111; exported 0 to 0.24 seconds.
- Sampled activity on the `oct6` source mesh.
- Kept the complete FreeSurfer pial mesh as the independent render domain.
- Mapped every render vertex to a hemisphere-local oct6 spherical triangle with three barycentric weights.
- Centered both hemispheres together and applied one shared uniform scale, preserving the anatomical aspect ratio.
- Filled inverse-excluded mesh vertices by nearest graph propagation and applied 5 neighbor-averaging display steps.

## License And Attribution

- The pinned OpenNeuro dataset declares CC0.
- Acknowledge Alexandre Gramfort and Matti Hämäläinen and cite the MNE publications requested by the dataset metadata.

## Notes

- dSPM is a model-derived, dimensionless, noise-normalized source estimate; it is not a direct measurement of neuronal firing.
- This script writes only to `.cache/datoviz/examples/cortical_activity` and does not modify the `data` submodule.
