# **README: Feature Engineering for Pneumonia Detection using Chest X-Rays**

## **Project Overview**

This project focuses on the feature engineering process for a machine learning model aimed at pneumonia detection in chest X-ray images. The goal is to extract meaningful features from the images and evaluate their relevance in distinguishing between pneumonia and normal images. This project walks through various image processing techniques, such as edge detection, texture extraction, and dimensionality reduction, and uses statistical analysis to determine which features significantly contribute to the classification.

## **Table of Contents**

- [Project Setup](#project-setup)
- [Image Preprocessing](#image-preprocessing)
- [Feature Engineering](#feature-engineering)
- [Statistical Analysis: T-test](#statistical-analysis-t-test)
- [Results and Discussion](#results-and-discussion)
- [Conclusion](#conclusion)
- [References](#references)

## **Project Setup**

Before running the code, make sure to have the necessary libraries installed. This project primarily uses the following Python packages:

- `numpy`
- `matplotlib`
- `scipy`
- `sklearn`
- `opencv`
- `pandas`

You can install the required libraries using `pip`:

```bash

pip install numpy matplotlib scipy scikit-learn opencv-python pandas


The dataset used consists of chest X-ray images, with 300 images in each category (pneumonia and normal). These images are loaded and preprocessed in the code.

Image Preprocessing
The first step in the project was image preprocessing. This included the following steps:

Resizing: Each image was resized to a uniform shape to ensure consistency across all images.
Grayscale Conversion: Images were converted to grayscale to simplify feature extraction.
Normalization: Pixel values were scaled between 0 and 1 to standardize the data.
Edge Detection: Techniques like Canny edge detection were used to highlight key structural features of the images that are potentially important for classification.
Image Preprocessing Code:
python
Copy
Edit
import cv2
import numpy as np

# Resize and normalize the image
def preprocess_image(image_path):
    image = cv2.imread(image_path)
    gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
    resized_image = cv2.resize(gray_image, (256, 256))  # Resize for consistency
    normalized_image = resized_image / 255.0  # Normalize to range [0, 1]
    return normalized_image
Feature Engineering
Feature extraction involves identifying key characteristics from the images that can help classify the images as either normal or pneumonia. Several techniques were used to extract features:

Texture Features: Statistical texture measures such as contrast, correlation, energy, and homogeneity were extracted using methods like the Gray-Level Co-occurrence Matrix (GLCM).

Edge Features: Edge features were captured using edge detection techniques, including Canny edge detection. These help identify the boundaries and shapes within the image, which are crucial for distinguishing between different types of X-ray images.

Thresholding: Otsu’s method was used for automatic thresholding to segment the images and highlight key regions of interest.

Skeletonization: The skeletonization technique was used to reduce the shapes in the image to their simplest form, preserving the essential features like borders and shapes while eliminating unnecessary details.

Principal Component Analysis (PCA): PCA was applied to reduce the dimensionality of the extracted features while preserving the most important information for classification. This helps in improving the efficiency of the model.

Feature Engineering Code:
python
Copy
Edit
from skimage.feature import greycomatrix, greycoprops

# Extract texture features
def extract_texture_features(image):
    glcm = greycomatrix(image, distances=[1], angles=[0], symmetric=True, normed=True)
    contrast = greycoprops(glcm, 'contrast')[0, 0]
    correlation = greycoprops(glcm, 'correlation')[0, 0]
    energy = greycoprops(glcm, 'energy')[0, 0]
    homogeneity = greycoprops(glcm, 'homogeneity')[0, 0]
    return contrast, correlation, energy, homogeneity
Statistical Analysis: T-test
Once the features were extracted, a statistical test was performed to evaluate which features were significant in differentiating between pneumonia and normal X-ray images. The T-test was used to compare the mean values of each feature between the two classes (pneumonia and normal).

T-test: The T-test was applied to each feature to assess if the mean difference between the two classes was statistically significant. Features with a p-value lower than 0.05 were considered significant.
T-test Code:
python
Copy
Edit
from scipy.stats import ttest_ind

# Perform T-test on extracted features
def perform_ttest(feature_set_1, feature_set_2):
    t_stat, p_value = ttest_ind(feature_set_1, feature_set_2)
    return t_stat, p_value
Results and Discussion
After conducting the T-test, we found that almost all of the features showed statistically significant differences between the pneumonia and normal categories. The exception was the contrast feature, which had no significant difference and will likely be excluded in future models.

Key findings include:

Significant Features: Texture-based features like correlation, energy, and homogeneity showed strong distinguishing power between pneumonia and normal X-rays.
Exclusion of Contrast: Contrast did not show a significant difference, and hence, it does not contribute meaningfully to the classification task.
Conclusion
This project demonstrated the importance of feature engineering in improving the performance of machine learning models. Through extensive preprocessing, feature extraction, and statistical analysis, we were able to identify meaningful features for pneumonia detection. While some features, like contrast, were not helpful, others significantly contributed to the classification task.

In the future, these features could be incorporated into a machine learning model, such as a convolutional neural network (CNN), to improve the accuracy of pneumonia detection in chest X-ray images.

The challenges faced during the project, including time constraints and limited knowledge of feature engineering techniques, helped me grow as a data scientist. With the skills gained, I feel confident in tackling similar projects in the future.

References
The following resources were instrumental in completing this project:

300 images per category
Feature Engineering Start
PCA Implementation
Random Sampling of Pneumonia Images
Convolutional Display
Otsu Threshold Format
Canny Edge Detection Ratio and Format
Skeletonization Techniques
T-test Application
pgsql
Copy
Edit
