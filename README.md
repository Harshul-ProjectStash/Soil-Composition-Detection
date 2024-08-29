# Soil-Composition-Detection
Development of a Gaussian Process Regression Model for Soil Composition Prediction Using Multispectral Image Analysis
This repository contains the code, reports, and related files for the project titled "Development of a Gaussian Process Regression Model for Soil Composition Prediction Using Multispectral Image Analysis." The project focuses on predicting soil composition (sand, silt, and clay proportions) using multispectral image data captured by a Parrot Sequoia camera. The approach integrates image preprocessing, feature extraction, dimensionality reduction using Fast PCA, and predictive modeling using Gaussian Process Regression (GPR).

## Project Overview
This project aims to develop an efficient model for soil composition prediction based on multispectral image analysis. The primary objectives include:

Collecting multispectral image data for soil samples.
Preprocessing images by cropping and separating spectral bands.
Dividing images into subblocks and extracting features using Gram matrix construction.
Applying Fast PCA for dimensionality reduction.
Developing and training a Gaussian Process Regression model to predict sand, silt, and clay proportions.
Classifying soil types using an empirical triangle based on predicted compositions.

## Dataset Details
The dataset consists of 62 distinct soil types, each with 3 samples, captured across 7 spectral bands. The multispectral images were preprocessed and divided into 10 subblocks per image.

## Methodology
The methodology involves several key steps:

Image Preprocessing: Automated cropping and spectral band separation.
Feature Extraction: Gram matrix construction capturing spectral relationships within subblocks.
Dimensionality Reduction: Fast PCA applied to reduce feature dimensions while retaining critical variance.
Predictive Modeling: Gaussian Process Regression (GPR) used for predicting soil composition.
Classification: Soil classification performed using the empirical triangle based on predicted proportions.
For more details, refer to the final_report.pdf

## Results and Discussions
The model achieved a Mean Squared Error (MSE) of 0.0049, demonstrating high accuracy in predicting soil composition. Detailed performance metrics, error analysis, and practical implications are discussed in the report 

## References
Gopi, E. S., & Palanisamy, P. (2013). Fast computation of PCA bases of image subspace using its inner-product subspace. Applied Mathematics and Computation, 219(12), 6729-6732. https://doi.org/10.1016/j.amc.2013.01.060

Gopi, E. S. (2020). Pattern Recognition and Computational Intelligence Techniques Using Matlab. [Publisher details if available].

Refer the complete code pdf to view code only of the project


