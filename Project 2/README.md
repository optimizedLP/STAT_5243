# Project 2: Cell Segmentation Classifier(Random Forest Model)

## Overview
This project involves training a machine learning model to classify cellular images using the **Random Forest Classifier**. The dataset consists of images from two categories: **DMSO** (control) and **treated** cells. The images are pre-processed and split into batches for training and evaluation. The model predicts whether a cell belongs to the **DMSO** or **treated** category based on extracted features.


## Features
- **Random Forest Classifier**: Utilizes the Random Forest algorithm for classification.
- **Data Preprocessing**: The dataset is processed in batches to prevent memory overflow and to optimize training.
- **Model Evaluation**: Includes the calculation of classification metrics and visualization of the confusion matrix.
- **Batch Processing**: Supports processing of large datasets in smaller, manageable batches.
  
## Data Preparation
The data used for training consists of pre-processed cell images categorized into **DMSO** and **treated** classes. You need to specify the directory containing these image files and a metadata file describing each image.


## Conclusion
The trained model outputs predicted treatment for test images.  
