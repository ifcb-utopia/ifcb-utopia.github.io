---
title: azure_blob_tools.py
layout: default
nav_order: 4
parent: utopia-pipeline-tools
grand_parent: Repositories
---

# azure_blob_tools module   

## Functions:

### list_containers_in_blob(connection_string=config_info['connection_string'])

Returns a list of the ifcb image containers in the specified Azure Blob storage.

#### Parameters:
- connection_string (str): The blob connection string. Default is None, so an input is required.

#### Returns:
- blob_containers (list): List of containers in the specified Azure blob.

### def list_files_in_blob(container, connection_string=config_info['connection_string'], selection='png'): 

Returns a Pandas dataframe of filepaths of all files in the specified blob container, or only images or csv files depending on the 'selection' parameter. 

#### Parameters:
- container (str): Specifies the name of the blob container
- connection_string (str): The blob connection string. Defaults to None, so input required.
- selection (str, kwarg): Indicates which files to select, default is 'png' which returns only image files, but other options are 'csv' and 'all' to return csv files and all files, respectively. 

#### Returns:  
- png_df (DataFrame): If selection is 'png', the function returns a dataframe of filepaths with '.png' in the string. Column name 'filepath'.
- csv_df (DataFrame): If selection is 'csv', the function returns a dataframe of filepaths with '.csv' in the string. Column name 'filepath'.
- all_df (DataFrame): If selection is 'all', the function returns a dataframe of all filepaths in the blob container, regardless of type. Column name 'filepath'.

### create_container(container_name, connection_string=config_info['connection_string']):

Creates a new container in the Azure Blob storage. Requires AzCopy setup. This function has not been tested. 

#### Parameters:
- param container_name (str): The name of the new container.

### upload_images_to_blob(container_name, local_directory_path, blob_storage_name=config_info['blob_storage_name']):

Upload a folder to the Azure Blob storage. This function has not been tested and likely needs edits. 

- container_name (str): Indicates which blob container the images will be uploaded to.
- local_directory_path (str): The path to the ml folder.