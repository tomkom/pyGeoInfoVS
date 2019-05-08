# pyGeoInfoVS - A Python Geographical information vizualization shootout 

Setting up a comparison of current Open Source (any licence) Python visualization options and allowing for their comparison. 

This shootout has been put up here by me (Martin Tomko, @dinomirMT, www.tomko.org)

Work in progress, please contribute. PLease clearly state in your contributions (in paritcular, full notebooks) some identifying/contact parameters, and possibly if you are a maintainer of the demonstrated packages.

Also add your contribution name up here (Name, handle, contribution)

I will try to produce a workshop/conference (one of the GIScience conferences, I would assume, or possibly a FOSS4Gxx one) writeup from this, with shared authorship form contributors.

## Aims

Provide a resource for selecting and using the right visualization library in Python 3.5+ for a range of common spatial science workflows.

As an absolute non-negotiable requirement, it must be possible to execute all of the stories below in a single consistent environment, with sorted dependencies (Python 3.5+, singel version of GDAL across the lot, usable for pyproj, geopandas, rasterio, etc.)

## Motivation - a personal take

This excercise is based on a few main sore points many of use experience:

- We need to teach beginner GIScience students how to make reasonable spatial visualizations, as part of a Spatial Information Programming course. This is not a core spatial visualization course, we have maybe 2 hours for visualization and the need to integrate some map outputs, and some statistical graphs throughout. 
- W need to provide some relatively appealing maps for research publications. This research is typically NOT about visualization, so meaningful defaults or simple way to add all necessary parameters is necessary. Visualization magicians would certainly produce better outputs with maual tweakings, but that is typically not needed to demonstrate whether our contributions are meaningful and work.

In both of these use cases, I am sick and tired of patching a single story based on a heterogenous assortment of libraries that I have to use - I would like one library that somehow covers most (not all). In teaching, this is an absolute requirement, in particular as it is a nightmare to maintain teaching materials and code from eyar to year, and track the maturity of libraries. 

This is reflected in the variety of Python viz libraries, referenced here: https://www.anaconda.com/python-data-visualization-2018-why-so-many-libraries/

Variety is great - but pragmatic decisions include ease of API, consistency, active maintenance, and others.

As an etalon, the consistency and readability of the ggplot ecosystem (R) is sought. That has a learning curve as well, of course, but the idioms are consistent.

## Approach

1. A set of notebooks replicating the same basic workflow, with the same data. If the provided data are not enough, please contribute other ( and note which notebooks need to be updated to use them). A workflow to produce pickles from the standard spatial data formats will be provided.

2. Each notebook can showcase additional capabilities, under a header 'Other capabilities'. These may be transferred to the main set if someone is able to replciate them for more than a single framework.

3. The aim here is to provide an educational resource. Code readability and succinctness are therefore paramount. While much may ba accomplished with advanced code magic, hidden unde a 'fancyVizFunction(mydata)', this is not desirable. Pythonic code, and only justified use (possibly well commented) of advanced labda fucntions, list comprehensions beyond common use for students with say half a term of Python exposure are discouraged.

4. This is not about data preparation and re-formatting. It should be possible to produce outputs based on the standard, provided, spatial data. Any additional data processing can happen ( e..g, for aesthetic reasons) in a separate notebook section. The data inputs for the visualization must be ready before thrown into the visualization production code.

## Compared capabilities - Print quality static spatial visualizaitons

### Core static capabilities

- Read in spatial data in lon/lat
- Display in WGS84/Web pseudomercator (renders any coordinates values as they are, projection is done in data wrangling pipeline)
- Apply styling to lines, points, polygons, or raster
- Add pre-rendered basemap
- BOLTSS (border, orientation, legend, title, scale, source)
- Export to graphics file in print quality
- Easily displays in jupyter notebook

### Nice to haves (static spatial visualizations)

- Parameter-based reprojection of data
- Graticules, meridian lines
- Plot together with other info plots
- Faceted plot ( e.g., by time)
- Export vectors in a vector format, for post-processing in Inkscape or similar
- 3D oblique view
- Animated gif exports for animations

## Compared capabilities - Dynamic spatial visualizations

### Core dynamic capabilities

- dynamic zoom and pan
- pop-ups to query data
- controls (via widgets in jupyter)

### Nice to haves (dynamic spatial information visualizations)

- brushing/interaction with other info-viz
- dynamic change of transparency and other visual parameters (sizes of symbols, colours)
- zoom dependent display of data

### Other considerations

1. Scales well (performance with progressively large datasets)

## Data

Data with a permissive, open licence will be used.

We need, for the same region (best, two sets of data - global and city scales)

### Vector data
- POI data
- a point layer, to assess visual clutter, point styling, etc (distinct to POI data, in some respect)
- Linear data (roads, train lines)
- Polygonal data (building footprints)
- thematic polygon data (Aggregate census data ,for choropleth maps)
- Contour lines
- Trajectory data 
- Mesh?
- 3D buildings

### Raster data

- Sattelite imagery
- Rendered basemap tiles endpoint
- DEM data
- thematic raster layer (Landuse/landcover type dataset)

## Compared libraries (add links):
I think as we start drawinfg conclusions, we may start awarding 0-5 satrs to these below...
I would also add date of last release, and date of last commit, based on github. NOt sure if this can be automatically updated in some simple way.

### Static:
- Matplotlib (without Basemap - dead branch of the project?). Most others build on matplotlib, so this is clearly going to be the leader, but the ease of interface note above matters.
- Cartopy
- Geopandas plot
- Geoplot (https://github.com/ResidentMario/geoplot)
- Geoplotlib (https://github.com/andrea-cuttone/geoplotlib ), requires pyglet 
- Geoviews
- splot (github.com/pysal/splot)
- rasterio
- QGIS NetAPI (?)
- xarray_dev (rasters)


### Dynamic:

- Folium
- ipyLeaflet (https://github.com/jupyter-widgets/ipyleaflet)
- mplleaflet
- Dash + plotly (Is this OS? Can this do maps? Or is this general purpose viz https://dash.plot.ly/)

### General purpose viz environments

- matplotlib
- altair
- bokeh
- branca
- ggplot (https://pypi.org/project/ggplot/ )
- seaborn ()
- pygal
- altair
- leather (https://leather.readthedocs.io/en/0.3.3/)
- Holoviews
- Netwokrx/igraph (often usable for spatial, but out of consideration here - assuem we can compute the netowkr parameters and store as attribute, we just want to plot the map now)



## Resources:

### Mapp related
- https://automating-gis-processes.github.io/2018/lessons/L5/overview.html
- http://darribas.org/gds18/labs/Lab_03.html 
- https://blog.ouseful.info/2019/04/02/fragment-components-for-rolling-your-own-gis-inside-jupyter-notebooks/


### General viz libraries:

- https://www.fusioncharts.com/blog/best-python-data-visualization-libraries/
- https://towardsdatascience.com/the-next-level-of-data-visualization-in-python-dd6e99039d5e


