# Project 3: U-Net Medical Imaging Segmentation

## Overview
This project focuses on developing a deep learning model for automating the segmentation of gastrointestinal organs in MRI scans. The goal is to assist radiation oncologists in efficiently segmenting the stomach and intestines for radiation therapy, thereby improving the speed and accuracy of cancer treatment.

Inspired by a past UW-Madison Kaggle competition, we implemented and evaluated deep learning models for medical imaging segmentation, specifically using U-Net and DeepLabV3.

## Table of Contents
- [Introduction](#introduction)
- [Data Description](#data-description)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Model Development and Evaluation](#model-development-and-evaluation)
- [Results and Discussion](#results-and-discussion)
- [Conclusion and Future Work](#conclusion-and-future-work)
- [Code and Models](#code-and-models)

## Introduction
The goal of this project is to automate the segmentation of gastrointestinal organs in MRI scans, helping radiation oncologists expedite the segmentation process and make more accurate decisions during cancer treatment. The project uses deep learning techniques, particularly U-Net and DeepLabV3, to perform semantic segmentation of MRI images.

## Data Description
The dataset used for this project consists of anonymized MRI scans from the UW-Madison Carbone Cancer Center. The images are in 16-bit grayscale PNG format, and each case includes multiple scan slices. The dataset also includes:
- **train.csv**: Contains IDs and RLE-encoded masks for training objects.
- **train/**: A directory with case/day subfolders containing MRI slice images.

### Key Data Preprocessing Steps
- Conversion of RLE-encoded masks to binary masks.
- Normalization of 16-bit grayscale images.
- Data augmentation techniques such as rotation, flipping, and scaling.
- Extraction of features from image paths and integration into a unified DataFrame.

## Exploratory Data Analysis (EDA)
EDA was performed to understand the distribution of data, including segment distribution across cases and days. Key observations:
- The number of slices per case varied.
- There was an imbalance in the number of organ pixels vs. background pixels in the dataset.

### Visualizations
![Distribution of Segments Across Cases](https://github.com/optimizedLP/STAT_5243/blob/main/Project%203/figures/%23%20of%20segments.png)
![Distribution of Mask Types](https://github.com/optimizedLP/STAT_5243/blob/main/Project%203/figures/mask%20types.png)

## Model Development and Evaluation

### Models Implemented
- **Baseline Model**: Rule-based thresholding methods.
- **Proposed Model**: A deep learning model using U-Net for semantic segmentation.

### Model Architectures

#### U-Net Overview
- Encoder with 5 stages of increasing feature channels.
- Decoder with upsampling layers and skip connections.
- Final output layer with a 1x1 convolution to generate the 3-channel output.

#### DeepLabV3 Overview
- Atrous Spatial Pyramid Pooling (ASPP) for multi-scale feature extraction.
- Backbone typically using ResNet or MobileNetV2.
- A head combining ASPP features and refining segmentation maps.

### Performance Metrics
The models were evaluated using the following metrics:
- **Dice Coefficient**: Measures the similarity between predicted and actual segmentation.
- **3D Hausdorff Distance**: Quantifies the distance between predicted and actual segmentation boundaries.

| Model          | Dice Coefficient | 3D Hausdorff Distance |
|----------------|------------------|-----------------------|
| Baseline Model | 0.65             | 30.5                  |
| Proposed Model | 0.87             | 12.3                  |

## Results and Discussion
The proposed deep learning model (U-Net) significantly outperformed the baseline model, achieving a Dice coefficient of 0.87 and a lower 3D Hausdorff distance. The model demonstrated high accuracy in segmenting the gastrointestinal organs.

### Model Output Visualizations
![Segmentation Model Output](https://github.com/optimizedLP/STAT_5243/blob/main/Project%203/figures/seg%202.png)
![U-Net Output](https://github.com/optimizedLP/STAT_5243/blob/main/Project%203/figures/unet%201.png)
![Final Segmentation Output](https://github.com/optimizedLP/STAT_5243/blob/main/Project%203/figures/final%20segmentation.png)

## Conclusion and Future Work

### Conclusion
- Data preprocessing and EDA helped in understanding the challenges of medical image segmentation.
- The U-Net model outperformed the baseline model with high accuracy.
- The project demonstrated the effectiveness of deep learning in automating segmentation tasks for clinical applications.

### Future Work
- Implement model explainability techniques like SHAP or LIME.
- Integrate additional clinical metadata (e.g., tumor location) to improve model performance.
- Extend the analysis to larger and more diverse datasets for broader applicability in clinical settings.
