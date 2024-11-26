# Project 2: Cell Segmentation Classifier(Random Forest Model)


[Project Report](https://github.com/optimizedLP/STAT_5243/blob/main/Project%202/report/STAT5243_Project_2.pdf)
## Overview
This project involves training a machine learning model to classify cellular images using the **Random Forest Classifier**. The dataset consists of images from two categories: **DMSO** (control) and **treated** cells. The images are pre-processed and split into batches for training and evaluation. The model predicts whether a cell belongs to the **DMSO** or **treated** category based on extracted features.


## Features
- **Random Forest Classifier**: Utilizes the Random Forest algorithm for classification.
- **Data Preprocessing**: The dataset is processed in batches to prevent memory overflow and to optimize training.
- **Model Evaluation**: Includes the calculation of classification metrics and visualization of the confusion matrix.
- **Batch Processing**: Supports processing of large datasets in smaller, manageable batches.
  
## Data Preparation
The data used for training consists of pre-processed cell images categorized into **DMSO** and **treated** classes. You need to specify the directory containing these image files and a metadata file describing each image.

## Cell segmentation & Feature extraction using Cellpose
#### Figure 1: Original Image VS Predicted Cellpose Outlines
![cellpose 1](https://github.com/optimizedLP/STAT_5243/blob/main/Project%202/figures/Screenshot%202024-11-26%20111328.png)
#### Figure 1: Predicted Mask VS Predicted Cellpose
![cellpose 2](https://github.com/optimizedLP/STAT_5243/blob/main/Project%202/figures/Screenshot%202024-11-26%20111429.png)


## Conclusion
The trained model outputs predicted treatment for test images.  
#### Figure: Output
![Model output with treatments](https://github.com/optimizedLP/STAT_5243/blob/main/Project%202/figures/Screenshot%202024-11-26%20122634.png)
