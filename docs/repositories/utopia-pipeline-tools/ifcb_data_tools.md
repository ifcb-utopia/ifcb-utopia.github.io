---
title: ifcb_data_tools.py
layout: default
nav_order: 7
parent: utopia-pipeline-tools
grand_parent: Repositories
---

# ifcb_data_tools module

Contains funcitons to work with locally hosted IFCB images and processed ml folders. 

### Imports:
- os
- re

### Functions:

#### `retrieve_filepaths_from_local(folder_location)`:
Retrieves filepaths of all IFCB images in the specified processed data folder location (local). Returns a list of all image filepaths in the ml sub-folders.

##### Parameters:
- folder_location (str): Filepath to the ml folder location.

##### Returns:
- image_list (list): List of all IFCB image filepaths in a given local folder.