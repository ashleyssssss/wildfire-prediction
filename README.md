# Repository Description
This repository contains the codebase and models developed for our research project on wildfire prediction using deep learning, specifically Convolutional Neural Networks (CNNs). The project uses MODIS satellite imagery and implements several lightweight CNN architectures to predict wildfire risk or presence.
# File Descriptions
### DataCollection.ipynb -- Vince Guan
This script handles data loading, cleaning, preprocessing and label generation. It reads MODIS image data, processes it into the required format (e.g., resizing, normalization), and prepares the dataset for training and validation.

Run this first to prepare the data needed for training.
### cal_fires_32x32.npz
Data from the California region, used to test the generalisation ability of the best model.
### models_cv.ipynb -- Yunfan Sun, Sining Zhu, Lan Wang, Houlan Dai, Bimo Danindro
This is the main training and evaluation script. It includes: 
- Model architecture definitions (Six models)
- Cross-validation setup
- Hyperparameter tuning
- Training and performance evaluation
- Generalisation on the new dataset

This is the script used to replicate our results.
### best_cnn_model.keras 
This is the saved model (in Keras format) that achieved the best performance across all tested architectures. Load this model to reproduce the results consistent with those in the report.

---------------------
Before our task type is converted to a classification task, our attempts at the encoder-decoder structure are shown in the following file：
### Modification_Loss.ipynb (Deprecated) -- Bimo Danindro
Earlier experiment using ResNet50V2 and custom loss functions (Focal + Dice). No longer maintained or reproducible due to task shift (segmentation → classification).

### attention_mechanism.ipynb (Deprecated) -- Sining Zhu
Previously explored encoder-decoder architecture with attention for semantic segmentation. Also not compatible with the current dataset or problem formulation.



