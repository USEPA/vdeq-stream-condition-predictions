# vdeq-stream-condition-predictions
The vdeq-stream-condition-prediction repository is for making spatial stream network predictions of stream condition in the James River watershed in Virginia. The data come from Probabilistic Monitoring by Virginia Department of Environmental Quality that is used in a spatial stream network (SSN) analysis.
Independent data collected from 2019-2022 is used to test predictions of the spatial stream network model built based on 2001-2018 data.

# Instructions

## Scripts
This repository is broken principally into 6 scripts. These scripts are numbered in the main directory from 01-06 and should be performed in order. 

01_Semivariogram.Rmd - Primary Focuses:
* Reading and Writing Spatial Data
* Summarizing Distances
* Semivariogram Clouds and Semivariogram Plots
* Randomization of Semivariograms

02_Torgegram.Rmd - Introducing the user to the idea of a Torgegram and it's uses.

03_Y-Intercept_SSN_Model.Rmd - Prepare a spatial stream network model without any covariates. Looking purely at the spatial structure of the data. 

04_StreamCat_Covaritates_and_SSN_Object.Rmd - Explore the introduction of EPA's Stream Catchment dataset into the SSN object for additional variable availability. 

05_MLR_SSN_Model.Rmd - Introduce the idea of a multiple linear regression model to the SSN object, and incorporate variable selection methods.

06_SSN_Model_Predict.Rmd - Produce predictive results based on models identified in script 05, based on new data. 

## Data 

This repository currently relies upon an SSN object generated for the James River Watershed in Virginia. This object is James_071024_pluspreds.ssn in the ssn_object/ folder. 
Additionally multiple datasets are available in the data/ folder and are pulled in various locations throughout the 6 main scripts. 

## Packages
There are a relatively large number of packages required to run each of the 6 scripts, and are all called out at the beginning of their respectitive scripts. Additionally a sessionInfo() call output has been added to each script to provide the user with a list of all the package versions that were utilized in the creation of the script.

## Commented Code
In some of the scripts there are sections of code that are commented out. These sections are not necessary for the completion of the script, but are included for the user to explore and understand some of the additional EDA that was conducted in the process of creating this example.
