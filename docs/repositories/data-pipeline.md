---
title: data-pipeline
layout: default
nav_order: 2
parent: Repositories
---

# `data-pipeline`

This repository contains a set of marimo notebooks to streamline the data processing pipeline from raw IFCB images to CNN-classified datasets, with additional tools to set up PIVOT for validation. The pipeline steps are shown below:

# ![Pipeline_Diagram](/assets/images/Data_Pipeline_Diagram.png)  

## Notebooks

1. `create_dataset_csv.py`: Classifies all images in the `ml` folder that is created when converting raw IFCB data to png files with the CNN and produces a dataframe for analysis. Can be used with a folder of images stored locally or on the Azure blob. 
2. `pivot_sql_setup.py`: Runs all the necessary setup steps to create PIVOT and ingest the first set of data. Requires Azure blob storage and an Azure SQL database. This notebook also has the capability to add a new dataset to a pre-existing PIVOT SQL database.
3. `make_seabass.py`: Takes in metadata and the dataframe of classified labels and produces a folder of SeaBASS-formatted files that can be submitted to NASA. 

## Other Files

- `environment.yaml`: The file used to set up the ifcb-utopia Python environment. It contains all the packages needed to run the data-pipeline notebooks and PIVOT. 
- `global_val_setup.py`: A file containing template dictionaries for cloud tool configuration information and investigator names, organizations, and contact information. It also has a calibration ratio variable that can be edited from the default 2.7488 pixels/micrometer. This information needs to be added before running the notebooks. 

### Marimo  

I have chosen to use Marimo notebooks for this data pipeline. Marimo is an open-source, reactive Python notebook that can be run in notebook format, as a script, or as an app. Check out the Marimo website for more information: [https://marimo.io/](https://marimo.io/).

## Setup Steps

__IN PROGRESS__ 