---
title: data-pipeline
layout: default
nav_order: 3
has_children: true
parent: Repositories
---

# `data-pipeline`

This repository contains a folder of programs - `utopia_pipeline_tools` - and a set of marimo notebooks to streamline the data processing pipeline from raw IFCB images to CNN-classified datasets, with additional tools to set up PIVOT for validation. The pipeline steps are shown below:

# ![Pipeline_Diagram](/assets/images/Data_Pipeline_Diagram.png)  

## Notebooks

1. `process_raw_ifcb.py`: Converts a selected `raw` folder containing `.adc`, `.hdr`, and `.roi` files into an `ml` folder containing `.png` files. This notebook also includes an option to upload the resulting images to an Azure blob container.
2. `create_dataset_csv.py`: Classifies all images in the `ml` folder with the CNN and produces a dataframe for analysis. 
3. `pivot_sql_setup.py`: Runs all the necessary setup steps to create PIVOT and ingest the first set of data. Requires Azure blob storage and an Azure SQL database. This notebook only needs to be run if you are creating an entirely new database for PIVOT.
4. `pivot_data_ingestion.py`: Adds a new dataset to a pre-existing PIVOT SQL database and performs all necessary setup steps. 

### Marimo  

I have chosen to use Marimo notebooks for this data pipeline. Marimo is an open-source, reactive Python notebook that can be run in notebook format, as a script, or as an app. Check out the Marimo website for more information: [https://marimo.io/](https://marimo.io/).

## Setup Steps

__IN PROGRESS__ 