# Contiguous U.S. State Population Density Choropleth

## Source

- Boundaries: U.S. Census Bureau 2024 Cartographic Boundary File, states, 1:20m, `https://www2.census.gov/geo/tiger/GENZ2024/shp/cb_2024_us_state_20m.zip`.
- Population: U.S. Census Bureau Vintage 2025 state resident population estimates, `https://www2.census.gov/programs-surveys/popest/tables/2020-2025/state/totals/NST-EST2025-POP.xlsx`.

## Processing

- Filtered to the 48 contiguous U.S. states; Alaska, Hawaii, District of Columbia, Puerto Rico, and territories are excluded to avoid inset layout in the first gallery target.
- Projected longitude/latitude rings with a spherical Albers equal-area transform for the contiguous United States.
- Normalized projected coordinates into scene space and encoded each shapefile ring as one polygon-set region.
- Computed population density from 2025 resident population estimates divided by Census `ALAND` square meters.
- Stored `log10(people per km2)` as the displayed scalar value.
- Wrote flat typed arrays in `prepared/` so the C example only loads render-ready polygon-set data.

## License And Attribution

- U.S. Census Bureau public data may be reused; cite the Census Bureau as the source of original data.
- Generated Datoviz prepared files are derived from those public source datasets.

## Notes

- Interior holes are not preserved in the prepared polygon-set bundle; source rings are rendered as independent filled regions.
- Generated media should cite the U.S. Census Bureau boundary and population sources.
