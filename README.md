# **README: Feature Engineering for Pneumonia Detection using Chest X-Rays**

## **Project Overview**

This project focuses on the feature engineering process for a machine learning model aimed at detecting pneumonia in chest X-ray images. The objective was to extract meaningful features from the images and evaluate their relevance in distinguishing between pneumonia and normal X-rays. The process involved image preprocessing, feature extraction, and statistical analysis to identify which features contribute most to classification accuracy.

## **Tools and Libraries**

The following tools and libraries were used throughout the project:

- **Python**: Primary programming language for image processing, feature extraction, and statistical analysis.
- **NumPy**: For efficient handling of numerical data and mathematical operations.
- **Matplotlib**: Used for data visualization to plot and analyze the results.
- **SciPy**: For statistical analysis, including conducting the T-test.
- **OpenCV**: Used for image preprocessing tasks like resizing, grayscale conversion, and edge detection.
- **scikit-learn**: For machine learning tasks, particularly principal component analysis (PCA) for dimensionality reduction.
- **Pandas**: For managing and processing data, especially during statistical analysis.

## **Project Steps**

The project was divided into the following main steps:

### **1. Image Preprocessing**

- **Resizing**: All images were resized to a uniform shape to maintain consistency across the dataset.
- **Grayscale Conversion**: Conversion to grayscale helped simplify the analysis, as it reduced the image complexity without losing essential information.
- **Normalization**: Pixel values were scaled between 0 and 1 to standardize the data and improve model training.
- **Edge Detection**: Techniques like Canny edge detection were used to highlight structural features, such as the outline of the lungs, which may be crucial for detecting pneumonia.

### **2. Feature Engineering**

Key features were extracted from the X-ray images to help classify them as either "pneumonia" or "normal". The following techniques were used:

- **Texture Features**: Statistical measures like contrast, correlation, energy, and homogeneity were extracted from the images using the Gray-Level Co-occurrence Matrix (GLCM).
- **Edge Features**: Canny edge detection provided boundaries and shapes that could help differentiate between the two classes.
- **Dimensionality Reduction**: Principal Component Analysis (PCA) was used to reduce the number of features while maintaining the most important information.

### **3. Statistical Analysis (T-test)**

Once the features were extracted, a **T-test** was applied to determine which features had statistically significant differences between pneumonia and normal X-ray images. The T-test helped assess whether the mean differences between the two classes for each feature were large enough to matter. Features with a p-value less than 0.05 were considered significant.

## **Results and Discussion**

The statistical analysis revealed that most of the texture-based features, such as correlation, energy, and homogeneity, were highly significant in distinguishing pneumonia from normal X-rays. However, **contrast** did not show significant differences, and it was concluded that this feature would likely be excluded from future models.

## **Conclusion**

This project demonstrated the importance of feature engineering in improving the performance of machine learning models, especially in image classification tasks. By extracting and analyzing various image features, we were able to identify which aspects of the X-ray images contributed most to distinguishing between pneumonia and normal cases. The process also highlighted the value of statistical analysis in validating the relevance of features for a classification task.

In future work, these features can be used to train a machine learning model, such as a convolutional neural network (CNN), to further improve pneumonia detection accuracy. This project also reinforced the value of preprocessing and feature extraction in creating a strong foundation for machine learning applications.

## **Skills Gained and Applied**

Throughout this project, I gained valuable experience in several areas of data science and machine learning, including:

- **Image Preprocessing**: Techniques like resizing, grayscale conversion, and edge detection, which are essential in preparing data for analysis.
- **Feature Engineering**: The ability to extract and process various types of features from images to improve model performance.
- **Statistical Analysis**: Using the T-test to assess the significance of different features and ensure the reliability of the results.
- **Dimensionality Reduction**: Applying PCA to reduce the number of features while retaining the most important information for classification.

## **References**

The following resources were instrumental in completing this project:

- "Feature Engineering for Machine Learning" by Alice Zheng and Amanda Casari
- OpenCV Documentation for Image Processing Techniques
- SciPy Documentation for Statistical Analysis
- scikit-learn Documentation for Principal Component Analysis
- Image Preprocessing and Edge Detection Techniques in OpenCV
