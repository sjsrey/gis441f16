# QGIS-Plugin
# Analysis Document - Bivariate Choropleth Map
Quan Zhou ([UrsulaQuan])(https://github.com/UrsulaQuan)  
11-07-2016  

## Introduction
### Purpose  
1, To display two variables simultaneously and generate a more readable choropleth map.
2, To allow for estimation and trend analysis of the degree or spatial pattern of cross-correlation between variables. 

### Scope
1, Interface design.
2, The communication between UI and the polygon feature class.
3, Combine two data themes together into a hybrid map symbol.

### Objectives and Success Metrics
1, Read two fields in polygon feature’s attributes table.
2, Use Quantile classification method for continuous variable with visualized histograms.
3, Generate bivariate choropleth map legend.
4, Generate bivariate choropleth map.

## Current System
This QGIS Bivariate Choropleth Map plugin would be built based on PySAL visualization, but add multiple atrributes in mapping. The GeoVISTA toolkit bivariate mapping function is foucused on the spatial analysis and statistical realtionship between two attributes analysis. IndieMapper is well designed and developed online geovialization software, but is very slow and inconvenient to do a series of data analysis, visualization and map exporting operations. ArcGIS Bivariate Renderer is another visualiztion tool on ArcView with beautiful cholors scheme choices. The weakness is that legend is bad designed.

#### PySAL visualization
[PySAL visualization](http://pysal.readthedocs.io/en/v1.11.0/library/contrib/index.html?highlight=visualization) is the base of this plugin development. It provides the simple (use- and dependency-wise) and lightweight conversion of PySAL structures into commonly used visualizations. The functions contain the classification methodes and number, colors schmem choosing and choropleth map preview.

#### GeoVISTA-toolkit
[GeoVISTA-toolkit Bivariate Visualization](http://www.geovista.psu.edu/resources/flyers/GeoVizToolkit_InfoSheet_VACCINE_Kickoff.pdf) allows analysts to mix and match data visualization components to quickly construct custom analysis tools. Relationships among pairs of variables are explored with bivariate maps and graphs, while multivariate relationships are explored using matrixes of views (with many variables in pairwise views) and multivariate glyphs. 

#### IndieMapper
[IndieMapper](http://indiemapper.com/app/learnmore.php?l=multivariate) is one of the many free online mapping sites that could make static, thematic maps from geographic data by bringing the best of traditional cartographic design to internet map-making. In bivariate mapping module, it provides 6 ways of geovisualization: bivariate choropleth map, bivariate cartogram, biv. proportional symbols, value-by-alpha, proportional lables and colored proportional lables with standardizing data function.
#### ArcGIS Bivariate Renderer
[ArcGIS Bivariate Renderer](http://resources.esri.com/help/9.3/arcgisdesktop/com/samples/Cartography/Renderers/Bivariate_Renderers/73e5062c-16c5-4fa1-b18c-92022a6c4393.htm) is a plugin in ArcView. It consists of two custom bivariate renderers: ColorBivariateRend and ColorSzBivariateRend. In general, bivariate renderers are useful for representing the relationship between two data distributions. Two variables are classified independently, and their combination is represented using some combination of symbol color and size.

#### How will Bivariate Choropleth Map improve
1, The data source type
...
2, The legend style
...

## System Proposal
### Overview
This plugin will work as choroBrewer to provide users choices to pick up colors when design a bivariate map that reflect the relation ship of two attributes as well as display the space distribution pattern. All of operations will be in a new signle window: Data input, Map setting, Legend, Previvew of histograms and Preview of map.
### Functional Requirements
Listing of features to be implemented:
* Read attribute table content and dispaly needed information in interface
* Data Input
  1. Choose polygon feature class
  2. Choose fields of data to read
  3. Generate histograms to visualize the distributions
  4. Choose bivariate color scheme
* Mapping
  1. Generate bivariate legend
  2. Preview of choropleth map
  3. Generate new layer of bivariate choropleth map in QGIS
* User Interface: Operation panel and Preview panel in sigle dialog box

### Nonfunctional Requirements
#### Usability
For each button or drop list, there will be brief explanation at the bottom of dialog box. And the detailed helping documentation and user guide will also be attached in this tool.
#### Reliability
Any public version of the plugin should minimally avoid bugs after extensive tests. 
#### Performance
This plugin will generate two maps. The preview map will be showed in dialog box and response to users’ condition of data input. The output map will be showed in QGIS as a new layer, which would be changed in attribute table and symbology property.#### Supportability
Since this is an open source plugin project, all of questions, feedbacks and suggestions could be left on Github, which could be answered and solved by the developer.
#### Implementation
This single plugin will be implemented by Quan Zhou, but will be discussed and supervised by the GIS441 team.
#### Interface
This plugin will be showed in a new dialog box as a visualization tool to allow users to preview the bivariate attributes.
#### Packaging
All of package would be showed in Github and could be used when being forked, downloaded and placed in QGIS software.

## Project Management
#### Schedule and milestones
Date | Key features
--- | ---
Nov 15 | Read two attributes and generate two histograms
Nov 30 | Generate bivariate choropleth map legend and map
Nov 15 | Communication between interface and data
Dec 01 | Plugin on QGIS and test

#### Repository
URL for project repository: [project repository](http://git@github.com:UrsulaQuan/QGIS-Plugin.git)