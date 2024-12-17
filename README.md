# Predictive Modeling of Urban Heat Hotspots in Washington, DC
## PPOL 6803: Data Science for Public Policy
Authors: Madeleine Adelson, Stephanie Jamilla, and Jamie Jelly Murtha\
GitHub Pages Link: https://stejamilla.github.io/final-project/

This year, DC [reached a record high temperature](https://www.washingtonpost.com/weather/2024/07/16/dc-heat-100-record-high-temperatures/) of 104 degrees in July, matching a previous record in 1988 and after having gone eight years without breaking 100 degrees. This sparked wide public discourse about the adverse effects of heat on the health and safety of communities, some of whom may be disproportionately affected by the rising temperatures. 

In this project, we build three supervised machine learning models that predict whether or not one of DC's 571 block groups is part of an urban hot spot or not. The underlying outcome variable we aim to predict is the average summer evening temperature of DC taken from a 2020 DC urban tree canopy dataset and created by the[Sustaining Urban Places Research Lab (SUPR)](https://climatecope.research.pdx.edu/) at Portland State University in 2018. Predictor variables are drawn from the aforementioned tree canopy dataset, which contains additional data on landcover characteristics like non-canopy vegetation, impervious surface area, etc. We also use 2016-2020 American Community Survey data to leverage predictors about the population in each block group. 

We first build a decision tree model to determine whether or not a block group is a "hotspot" or "not hotspot." We define "hotspot" as a block group that has an average temperature at least one standard deviation above the mean temperature, in this case 91.6 degrees Fahrenheit. Second, we create linear regression and random forest models to predict what the average evening temperature is for a block group. We then assess the performance of these two models against each other and create predictions based on the more accurate one.

In order to replicate this project, you have to download the following datasets:
* Urban Tree Canopy by Census Block Group in 2020 (DC Open Data): [Download the Shapefile data type](https://opendata.dc.gov/datasets/DCGIS::urban-tree-canopy-by-census-block-group-in-2020/about)
* Urban Tree Canopy by Census Block Group in 2020 (DC Open Data): [Download the Shapefile data type](https://opendata.dc.gov/datasets/DCGIS::urban-tree-canopy-by-ward-in-2020/about)
  * This dataset is used to extract DC ward boundaries.
* 2016-2020 American Community Survey: [Get an API key here](https://api.census.gov/data/key_signup.html)
  * This is extracted using a Census API call in the r code. 


