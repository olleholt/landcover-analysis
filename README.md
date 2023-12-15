Author: Olivia Holt

*from MEDS course: eds223 week 9 lab*

## Overview

Monitoring the distribution and change in land cover types can help us understand the impacts of phenomena like climate change, natural disasters, deforestation, and urbanization. Determining land cover types over large areas is a major application of remote sensing because we are able to distinguish different materials based on their spectral reflectance.

Classifying remotely sensed imagery into landcover classes enables us to understand the distribution and change in landcover types over large areas. There are many approaches for performing landcover classification -- supervised approaches use training data labeled by the user, whereas unsupervised approaches use algorithms to create groups which are identified by the user afterward.

credit: this lab is based on a materials developed by Chris Kibler.

### Task

To use a form of supervised classification, a decision tree classifier. [Decision trees](https://medium.com/@ml.at.berkeley/machine-learning-crash-course-part-5-decision-trees-and-ensemble-models-dcc5a36af8cd) classify pixels using a series of conditions based on values in spectral bands. These conditions (or decisions) are developed based on training data. To create a land cover classification for southern Santa Barbara County based on multi-spectral imagery and data on the location of 4 land cover types:

-   green vegetation

-   dry grass or soil

-   urban

-   water

## Highlights of analysis:

-   load and process Landsat scene

-   crop and mask Landsat data to study area

-   extract spectral data at training sites

-   train and apply decision tree classifier

-   plot results

## Data

### Landsat 5 Thematic Mapper

-   [Landsat 5](https://www.usgs.gov/landsat-missions/landsat-5)

-   1 scene from September 25, 2007

-   bands: 1, 2, 3, 4, 5, 7

-   Collection 2 surface reflectance product

### Study area and training data

-   polygon representing southern Santa Barbara county

-   polygons representing training sites

    -   type: character string with land cover type

```         
landcover-analysis

│ landcover-analysis.Rmd

│ README.md

│

└───data
|
  └───landsat-data

    │ LT05_L2SP_042036_20070925_20200829_02_T1_SR_B1.TIF

    │ LT05_L2SP_042036_20070925_20200829_02_T1_SR_B2.TIF

    | LT05_L2SP_042036_20070925_20200829_02_T1_SR_B3.TIF

    | LT05_L2SP_042036_20070925_20200829_02_T1_SR_B4.TIF

    | LT05_L2SP_042036_20070925_20200829_02_T1_SR_B5.TIF

    | LT05_L2SP_042036_20070925_20200829_02_T1_SR_B7.TIF

│
  └───studyarea_training-data

    | trainingdata.dbf

    | trainingdata.prj

    | trainingdata.shp

    | trainingdata.shx
    
    | trainingdata.cpg
    
    | trainingdata.qpj

    | SB_county_south.dbf

    | SB_county_south.prj

    | SB_county_south.shp

    | SB_county_south.shx
    
    | SB_county_south.cpg
    
    | SB_county_south.sbx
    
    | SB_county_south.sbn

    | SB_validation_points.dbf

    | SB_validation_points.prj

    | SB_validation_points.shp

    | SB_validation_points.shx
    
    | SB_validation_points.qpj
```
