Author: Olivia Holt

*from MEDS course: eds223 week 9 lab*

## Overview

Monitoring the distribution and change in land cover types can help us understand the impacts of phenomena like climate change, natural disasters, deforestation, and urbanization. Determining land cover types over large areas is a major application of remote sensing because we are able to distinguish different materials based on their spectral reflectance.

Classifying remotely sensed imagery into landcover classes enables us to understand the distribution and change in landcover types over large areas. There are many approaches for performing landcover classification -- supervised approaches use training data labeled by the user, whereas unsupervised approaches use algorithms to create groups which are identified by the user afterward.

credit: this lab is based on a materials developed by Chris Kibler.

### Task

In this lab, we are using a form of supervised classification, a decision tree classifier. Decision trees classify pixels using a series of conditions based on values in spectral bands. These conditions (or decisions) are developed based on training data. In this lab we will create a land cover classification for southern Santa Barbara County based on multi-spectral imagery and data on the location of 4 land cover types:

green vegetation

dry grass or soil

urban

water

Summary

load and process Landsat scene

crop and mask Landsat data to study area

extract spectral data at training sites

train and apply decision tree classifier

plot results

Data

Landsat 5 Thematic Mapper

Landsat 5

1 scene from September 25, 2007

bands: 1, 2, 3, 4, 5, 7

Collection 2 surface reflectance product

Study area and training data

polygon representing southern Santa Barbara county

polygons representing training sites

type: character string with land cover type
