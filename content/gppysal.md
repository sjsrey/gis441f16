# Geoprocessing with PySAL

## Introduction
In this session we will explore the use of PySAL and friends to process various forms of geospatial data.

We begin with vector based files including:

- shapefiles
- geojson
- well known text
- change

We then move on to consider what are known as spatial weights that express geographical relationships between observational units. Here we will consider obtaining weights from some of the file types above, as well as reading and writing spatial weights file types directly.


## Dependencies
For this session you will need to have pandas installed (which you should already have via anaconda). If you did create a conda environemnt for the course you have to add pandas to that environment if you have not already done so.

You will also have to have jupyter notebooks installed, using the same logic as for pandas.


### Setting up remotes
Moving foward we want to ensure that your fork and local clones of the course repository are in sync. If you have not yet done so, complete the following steps

Clone your fork to your local computer (laptop)

 On your clone, add an upstream remote:
`git remote add upstream https://github.com/sjsrey/gis441f16.git`

Rebase your clone with the latest from upstream:
`git pull --rebase upstream master`

After working locally if you add commits, or just want to update your fork on Github you can do this with:
`git push origin master`



## Processing Vector Geospatial Data

https://github.com/sjsrey/gis441f16/blob/master/content/notebooks/01_data_processing.ipynb


## Spatial Weights

https://github.com/sjsrey/gis441f16/blob/master/content/notebooks/02_spatial_weights.ipynb
