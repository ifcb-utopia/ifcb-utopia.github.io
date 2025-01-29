---
title: cnn_tools.py
layout: default
nav_order: 6
parent: utopia-pipeline-tools
grand_parent: Repositories
---

# cnn_tools module

Functions to work with Keras CNNs used to classify IFCB phytoplankton images.

### Imports:  
- numpy
- cv2
- keras from tensorflow

### Functions:

---

#### `preprocess_input(image)`:
Takes in an IFCB .png (or list of IFCB .pngs) and resizes it to fit the 
input dimensions of the CNN.

##### Parameters:
- image (list): IFCB .png file or list of files.

##### Returns:
- rescaled_image (list): Rescaled IFCB image(s).

---

#### `load_local_model(json_file_path, h5_file_path):
Loads locally saved model as Tensorflow keras model.

##### Parameters:
- json_file_path (str): Path to local .json model file.
- h5_file_path (str): Path to local .h5 model weights file.

##### Returns:
- loaded_model (tf.keras.Model): Loaded keras model.

---

#### `load_cloud_model():
- Not yet written.

---

#### `predict_labels():
- Not yet written.

---