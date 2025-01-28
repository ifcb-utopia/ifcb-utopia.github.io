---
title: __init__.py
layout: default
nav_order: 2
parent: utopia-pipeline-tools
grand_parent: Repositories
---

# utopia-pipeline-tools \_\_init\_\_  

The \_\_init\_\_ file contains a bit of metadata, global values referenced by utopia-pipeline-tools functions, and templates of dictionaries that require user input.   

The metadata includes the version number, code author, and organization.  

Global attributes are a dictionary of labels and their numerical keys that correspond to the numerical outputs of the CNN code, and a dictionary of Aphia IDs (taxonomic identifiers) of each CNN label.  

|Numerical Key  |ifcbUTOPIA Label  |Taxonomic Name  | Aphia ID|  
|:---  | :--- | :--- | :---|
|0|Chloro|Chlorophyta|801|
|1|Cilliate|Ciliophora|11|
|2|Crypto|Cryptophyceae|17639|
|3|Diatom|Bacillariophyceae|148899|
|4|Dictyo|Dictyochophyceae|157256|
|5|Dinoflagellate|Dinophyceae|19542|
|6|Eugleno|Euglenoidea|582177|
|7|Unidentified_Living|Biota|1|
|8|Prymnesio|Prymnesiophyceae|115057|
|9|Inoperative|Inoperative|-9999|  


The remaining variables and dictionaries are the same templates in the `global_val_setup.py` file in the `data-pipeline` repository. Check out that page for more information.