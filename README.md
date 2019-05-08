# pyGeoInfoVS
A Geographical information vizualization shootout: setting up a comparison of current python visualization options and allowing for their comparison. Work in progress, please contribute.

## Aims

Provide a resource for selecting and using the right visualization library in Python 3.5+ for a range of common spatial science workflows.

As an absolute non-negotiable requirement, it must be possible to execute all of the stories below in a single consistent environment, with sorted dependencies (Python 3.5+, singel version of GDAL across the lot, usable for pyproj, geopandas, rasterio, etc.)

## Motivation - a personal take

This shootout has been put up here by me (Martin Tomko, @dinomirMT, www.tomko.org) based on a few main sore points:

- I need to teach beginner GIScience students how to make reasonable spatial visualizations, as part of a Spatial Information Programming course. This is not a core spatial visualization course, we have maybe 2 hours for visualization and the need to integrate some map outputs, and some statistical graphs throughout. 
- I need to provide some relatoively appealing maps for my research publications. This research is typically NOT about visualization, so meaningful defaults or simple way to add all necessary parameters is necessary. Visualization magicians would certainly produce better outputs with maual tweakings, but that is tuypically not needed to demonstrate whether my contributions are meaningful or work.

In both of these use cases, I am sick and tired of patching a single story based on a heterogenous assortment of libraries that I have to use - I would like one library that somehow covers most (not all). In teaching, this is an absolute requirement, in particular as it is a nightmare to maintain teaching materials and code from eyar to year, and track the maturity of libraries. 

As an etalon, the consistency and readability of the ggplot ecosystem (R) is sought. That has a learning curve as well, of course, but the idioms are consistent.

## Approach

1. A set of notebooks replicating the same basic workflow, with the same data. If the provided data are not enough, please contribute other ( and note which notebooks need to be updated to use them). A workflow to produce pickles from the standard spatial data formats will be provided.

2. Each notebook can showcase additional capabilities, under a header 'Other capabilities'. THese may be shuffled to the main set if someone is able to replciate them for more than a single framework.

3. The aim here is to provide an educational resource. Code readability and succinctness are therefore paramount. While much may ba accomplished with advanced code magic, hidden unde a 'fancyVizFunction(mydata)', this is not desirable. Pythonic code, and only justified use (possibly well commented) of advanced labda fucntions, list comprehensions beyond common use for students with say half a term of Python exposure are discouraged.

4. This is not about data preparation and re-formatting. It should be possible to produce outputs based on the standard, provided, spatial data. Any additional data processing can happen ( e..g, for aesthetic reasons) in a separate notebook section. The data inputs for the visualization must be ready before thrown into the visualization production code.

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
