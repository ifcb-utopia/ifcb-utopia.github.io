---
title: utopia-pipeline-tools
layout: default
nav_order: 3
has_children: true
parent: Repositories
---

# utopia-pipline-tools Python package

## Modules
- __\_\_init\_\_.py:__ Contains version information, a dictionary of classification labels and their corresponding numerical representations, a dictionary of Aphia IDs of each label group, the pixel: $\mu$ m ratio, and placeholder templates for a dictionary of configuration information and a dictionary of investigator names, organizations, and emails. 
- __analysis\_tools.py:__ Currently has no functions.
- __azure\_blob\_tools.py:__ Functions used to interface between python code and the Azure blob.   
- __classified\_to\_seabass.py:__ Contains a class that converts IFCB metadata and classification information into the SeaBASS format used by NASA. 
- __cnn\_tools.py:__ Functions to prepare IFCB images to be passed through the CNN and to load the CNN. 
- __ifcb\_data\_tools.py:__ Miscellaneous functions intended to work with IFCB data. 
