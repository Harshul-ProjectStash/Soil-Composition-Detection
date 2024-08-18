# Soil-Composition-Detection
Development of a Gaussian Process Regression Model for Soil Composition Prediction Using Multispectral Image Analysis 
Development of a Gaussian Process Regression Model for Soil Composition Prediction Using Multispectral Image Analysis
This repository contains the code, reports, and related files for the project titled "Development of a Gaussian Process Regression Model for Soil Composition Prediction Using Multispectral Image Analysis." The project focuses on predicting soil composition (sand, silt, and clay proportions) using multispectral image data captured by a Parrot Sequoia camera. The approach integrates image preprocessing, feature extraction, dimensionality reduction using Fast PCA, and predictive modeling using Gaussian Process Regression (GPR).

Table of Contents
Project Overview
Directory Structure
Installation and Setup
Dataset Details
Methodology
Results and Discussions
Usage Instructions
References
Project Overview
This project aims to develop an efficient model for soil composition prediction based on multispectral image analysis. The primary objectives include:

Collecting multispectral image data for soil samples.
Preprocessing images by cropping and separating spectral bands.
Dividing images into subblocks and extracting features using Gram matrix construction.
Applying Fast PCA for dimensionality reduction.
Developing and training a Gaussian Process Regression model to predict sand, silt, and clay proportions.
Classifying soil types using an empirical triangle based on predicted compositions.
Directory Structure
The repository is organized as follows:


├── data/
│   ├── raw_images/            # Original multispectral images
│   ├── processed_images/      # Cropped and preprocessed images
│   ├── subblocks/             # Divided image subblocks
│   └── results/               # Model predictions and evaluation metrics
├── src/
│   ├── preprocessing/         # Image preprocessing scripts
│   ├── feature_extraction/    # Gram matrix construction and Fast PCA
│   ├── modeling/              # GPR model development and training
│   └── classification/        # Soil classification using empirical triangle
├── reports/
│   ├── final_report.pdf       # Internship evaluation report
│   └── presentations/         # Presentation slides for project defense
├── appendices/
│   ├── code_snippets.md       # Important code snippets used in the project
│   └── additional_results/    # Supplementary results and visualizations
└── README.md                  # Project documentation
Installation and Setup
Clone the repository:
bash
Copy code
git clone https://github.com/yourusername/soil-composition-prediction.git
Navigate to the project directory:
bash
Copy code
cd soil-composition-prediction
Install the required Python packages:
Copy code
pip install -r requirements.txt
Dataset Details
The dataset consists of 62 distinct soil types, each with 3 samples, captured across 7 spectral bands. The multispectral images were preprocessed and divided into 10 subblocks per image. The dataset is stored in the data/ directory.

Methodology
The methodology involves several key steps:

Image Preprocessing: Automated cropping and spectral band separation.
Feature Extraction: Gram matrix construction capturing spectral relationships within subblocks.
Dimensionality Reduction: Fast PCA applied to reduce feature dimensions while retaining critical variance.
Predictive Modeling: Gaussian Process Regression (GPR) used for predicting soil composition.
Classification: Soil classification performed using the empirical triangle based on predicted proportions.
For more details, refer to the final_report.pdf in the reports/ directory.

Results and Discussions
The model achieved a Mean Squared Error (MSE) of 0.0049, demonstrating high accuracy in predicting soil composition. Detailed performance metrics, error analysis, and practical implications are discussed in the report and visualizations located in the appendices/ directory.

Usage Instructions
To run the full pipeline:

Preprocess the images:

python src/preprocessing/preprocess_images.py
Perform feature extraction:

python src/feature_extraction/extract_features.py
Train the GPR model:

python src/modeling/train_model.py
Generate predictions and classifications:

python src/classification/classify_soil.py
References
Gopi, E. S., & Palanisamy, P. (2013). Fast computation of PCA bases of image subspace using its inner-product subspace. Applied Mathematics and Computation, 219(12), 6729-6732. https://doi.org/10.1016/j.amc.2013.01.060
Gopi, E. S. (2020). Pattern Recognition and Computational Intelligence Techniques Using Matlab. [Publisher details if available].
Kempen, B., Brus, D. J., & Heuvelink, G. B. (2009). "Soil Texture Mapping Using Gaussian Process Regression." Geoderma, 151(3-4), 243-251.
Xie, X., & Zhang, J. (2010). "Image Segmentation Using Fast Principal Component Analysis." Pattern Recognition Letters, 31(5), 494-501.
