# Analysis Document - bknqgis
Ziqi Li [(c040120)](https://github.com/c040120)  
11-07-2016  

## Introduction
### Purpose  
Bknqgis is a QGIS plugin aims to leverage the role of QGIS in making interactive maps and charts using Bokeh python package. The main functionality of the plugin is to utilize QGIS layer, with both data and symbology, to create interactive web pages or embeddable web scripts that contain maps and/or charts.

### Scope
The scope of the plugin includes the design of UI, the communication between UI and QGIS layer, backend data transformation from QGIS layer to Bokeh readable format, and web Visualization using Bokeh.

### Objectives and Success Metrics
The primary objective of this plugin is to provide a user-friendly visualization tool for spatial analysts to easily create post-analysis maps and charts in a browser, and further distribute such visuals across the Internet. Metrics for success heavily rely on usability of the plugin. The goal is to allow QGIS users who are not familiar with web programming to easily create simple maps and charts to present their works. We also expect the number of downloads tracked on QGIS Plugins Repository could proof its popularity.

### Definitions and Terms
* **QGIS**: QGIS is a free and open source Geographic Information System (GIS)
* **Bokeh**: Bokeh is a Python interactive visualization library that targets modern web browsers for presentation.
* **UI**: User interface
* **OSM**: Open Street Map is an openly licensed map of the world being created by volunteers using local knowledge, GPS tracks and donated sources
* **OpenLayer3**: OpenLayer3 is an open source javascript library to load, display and render maps from multiple sources on web pages.
* **Leaflet**: Leaflet is an open-source JavaScript library for mobile-friendly interactive maps.
* **D3**: Data-Driven Documents(D3) is a JavaScript library for visualizing data.
    6. Overview

## Current System
When talking about the integration of web mapping and QGIS, there are many plugins [(e.g. OpenLayers Plugin)](https://plugins.qgis.org/plugins/openlayers_plugin/) intend to import basemaps from providers (e.g. Google Maps and OSM) to the QGIS as map layers. Then users could do processing, analysis and mapping based on the real world basemaps. The other way around is to export QGIS layer to GEOJSON and to crete a web map using javascript mapping libraries [(e.g. Leaflet](http://leafletjs.com), [OpenLayer3, ](https://openlayers.org) [and D3)](https://d3js.org). Under this realm, there are several plugins that serve the purposes.

#### Qgis2web
 [Qgis2web](https://plugins.qgis.org/plugins/qgis2web/), the successor of qgis2leaf and qgis-ol3, is able to  export your QGIS layer to an OpenLayers3 or Leaflet webmap. The exported interactive webmap could provide basic operations including zooming, panning, searching, clicking, etc. This plugin currently has over 100,000 downloads from [QGIS Plugins Repository](https://plugins.qgis.org).

#### Qgis2threejs
[Qgis2threejs](http://qgis2threejs.readthedocs.io) is a QGIS plugin to create a web page for viewing 3D map in a browser that supports WebGL. The web page is created using [three.js](https://threejs.org) javascript library. This plugin is primarily used in visualizing terrain data.

#### D3 Map Renderer
[D3 Map Renderer](https://github.com/sbenten/d3MapRenderer) is another plugin used to create web map by using d3.js JavaScript library. It exports geometry of QGIS layer to geojson/topojson as the data input into d3. The major problem of the plugin is that it doesn't export symbology of layer to the web but just the geometry. For example, when making choropleth map, user has to manually set colors without the support from QGIS.

#### How will bknqgis improve
Compared with qgis2web, bknqgis will have better user experience when interacting with maps without basemaps. There are certain situations that people don't need a basemap to provide the extra information about the location. Compared with D3 Map Renderer, bknqgis will not only export geometry of QGIS layer, but also, most importantly, the symbology of QGIS layer. In this way, it is way easier to work with colors and classifications in QGIS than in javascript and css.

Moreover, besides maps, another aspect of bknqgis is that it also can be used to create interactive charts. There are no QGIS plugins available now to make web charts to describe statistics and analytics behind the map.

## System Proposal
### Overview
The plugin export QGIS layer to a browser in either standalone html page or embeddable scripts. Consider the difference of map and all kinds of charts in Bokeh, they will be handled separately. User will be asked to select either creating a chart web page or map web page. Some common settings can be set such as background color and size. The UI will be in two panels. The left panel is used to do settings, and the right panel serves as a preview page.
### Functional Requirements
Listing of features to be implemented:
* Web page preview in dialog window
* Map
  1. Choose layer to export
  2. Choose attribute to be included in info window
  3. Set background color of the map
  4. Set size of the map
* Chart
  1. Choose type of the chart
  2. Choose data to be included in the chart
  3. Set background color of the chart
  4. Set size of the chart
* Choose either standalone html page or embeddable scripts
* User Interface - two panels

  ![alt text](ui.png)

### Nonfunctional Requirements
#### Usability
This plugin is maximizing easy-of-use by using user-friendly and intuitive UI design and having detailed documentation and user guide.
#### Reliability
Any public version of the plugin should minimally avoid bugs after extensive tests. The plugin will be well maintained and new version will be published periodically.
#### Performance
The plugin should be fast with layer with few and simple geometries. It might not be applied to layer with a lot of complicated geometries.
#### Supportability
Users could report any bugs, questions, and feedbacks to the developer either through GitHub page or email.
The developer will frequently answer questions and address issues.
#### Implementation
The build and test of the plugin will be implemented by Ziqi Li.
#### Interface
The input need is the layer in QGIS as long as it complies with QGIS layer class.
#### Packaging
The GitHub repository will be the whole package of the plugin. It should work if the user clone the repository and put it under the Plugins folder of QGIS.
#### Licensing
This plugin is developed under GNU GENERAL PUBLIC LICENSE Version 3, 29 June 2007. Copyright © 2007 Free Software Foundation, Inc. <http://fsf.org/> Everyone is permitted to copy and distribute verbatim copies of this license document, but changing it is not allowed.

## Project Management
#### Schedule and milestones
Date | Key features
--- | ---
Nov 19 | Basic interactive map can be exported
Nov 23 | Allow customization of map
Nov 28 | Create Moran's scatterplot
Dec 02 | Visualization is previewable in Plugin dialog UI

#### Repository
URL for project repository: [project repository](https://github.com/c040120/bknqgis)

## Useful Links
* QGIS: http://www.qgis.org/en/site/
* Bokeh: http://bokeh.pydata.org/en/latest/
* qgis2web: http://bokeh.pydata.org/en/latest/
* d3.js: https://d3js.org
* Leaflet: http://leafletjs.com
* QGIS Plugins Repository: https://plugins.qgis.org
