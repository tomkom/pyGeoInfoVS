# pyGeoInfoVS
A Geographical information vizualization shootout: setting up a comparison of current python visualization options and allowing for their comparison. Work in progress, please contribute.

## Aims

## Approach

1. A set of notebooks replicating the same basic workflow, with the same data. If the provided data are not enough, please contribute other ( and note which notebooks need to be updated to use them). A workflow to produce pickles from the standard spatial data formats will be provided.

2. Each notebook can showcase additional capabilities, under a header 'Other capabilities'. THese may be shuffled to the main set if someone is able to replciate them for more than a single framework.

## Compared capabilities - Print quality static spatial visualizaitons

### Core static capabilities

- Read in spatial data in lon/lat
- Display in WGS84/Web pseudomercator
- Apply styling to lines, points, polygons, or raster
- Add pre-rendered basemap
- BOLTSS (border, orientation, legend, title, scale, source)
- Export to graphics file in print quality
- Show in jupyter notebook

### Nice to haves (static spatial visualizations)

- Plot in facet by time
- Plot together with other info plots

## Compared capabilities - Dynamic spatial visualizaitons

### Core dynamic capabilities

- dynamic zoom and pan
- pop-ups to query data
- controls (via widgets in jupyter)

### Nice to haves (dynamic spatial information visualizations)

- brushing/interaction with other info-viz

### Other considerations

1. Scales well (performance with progressively large datasets)

## Data

## Compared 
