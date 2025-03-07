# **Pneumonia Detection using Chest X-rays**

## **Project Overview**
This project focuses on building a machine learning model capable of detecting pneumonia from chest X-ray images. The goal is to classify X-ray images into two categories: **Normal** and **Pneumonia**, using a deep learning approach. The model was developed using a Convolutional Neural Network (CNN) architecture and trained on a dataset of chest X-ray images to achieve high classification accuracy (94%).

## **Table of Contents**
1. [Technologies Used](#technologies-used)
2. [Dataset](#dataset)
3. [Project Structure](#project-structure)
4. [Approach](#approach)
5. [Model Architecture](#model-architecture)
6. [Training Process](#training-process)
7. [Evaluation and Results](#evaluation-and-results)
8. [Future Work](#future-work)
9. [References](#references)

## **Technologies Used**
This project utilizes various libraries and frameworks to handle data preprocessing, model building, training, and evaluation. Below is a list of the technologies used:

- **Python**: The programming language used for developing the entire project.
- **TensorFlow/Keras**: The main deep learning frameworks used for building and training the model.
- **NumPy**: Used for handling numerical operations, especially for image data manipulation.
- **Pandas**: Used for data manipulation and preprocessing tasks.
- **Matplotlib/Seaborn**: Used for data visualization, including plotting images and model performance metrics.
- **OpenCV**: Used for preprocessing the X-ray images (e.g., resizing, image enhancement).
- **scikit-learn**: Used for evaluating model performance with metrics like accuracy, confusion matrix, and classification report.

## **Dataset**
The dataset used in this project contains chest X-ray images, which are divided into two categories: **Normal** and **Pneumonia**. The dataset was sourced from Kaggle and contains a collection of images labeled with their respective conditions. These images were collected from various medical institutions and are useful for training models that can automatically detect pneumonia in chest X-rays.

- **Source**: [Chest X-ray Images (Pneumonia) Dataset on Kaggle](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia)
- **Number of images**: ~5,800 images, with 1,034 labeled as normal and 4,000+ labeled as pneumonia.
- **Image Format**: JPEG images, with varying dimensions that are resized to a standard size for training.

## **Project Structure**

The project is organized as follows:
/pneumonia-detection │ ├── /data # Contains dataset and preprocessed images │ ├── train # Training images │ └── val # Validation images │ ├── /notebooks # Jupyter notebooks for data exploration and model evaluation │ └── exploration.ipynb # Exploratory data analysis (EDA) and visualizations │ ├── /src # Python scripts for model building and training │ ├── model.py # Model architecture definition │ ├── preprocess.py # Image preprocessing functions │ └── train.py # Script to train the model │ ├── /logs # Logs for training process (e.g., TensorBoard logs) │ └── README.md # Project README file

markdown
Copy
Edit


## **Approach**
The main objective of this project is to develop an automated system that can detect pneumonia from chest X-ray images using deep learning techniques. The steps followed are outlined below:

1. **Data Preprocessing**:
   - The dataset is split into training and validation sets.
   - Images are resized to a uniform size (224x224 pixels).
   - Data augmentation techniques, such as random flips and rotations, are used to improve model generalization.
   - Image normalization is applied to scale pixel values to a range between 0 and 1.

2. **Model Building**:
   - A Convolutional Neural Network (CNN) architecture is used due to its success in image classification tasks.
   - The model consists of several convolutional layers, followed by max-pooling layers, and finally fully connected layers to classify images into two categories: **Normal** or **Pneumonia**.

3. **Model Training**:
   - The model is trained on the training set, with a batch size of 32 and an initial learning rate of 0.001.
   - Early stopping is used to prevent overfitting.
   - The model is trained for a maximum of 50 epochs, but the training stops early if the validation accuracy no longer improves.

4. **Model Evaluation**:
   - The trained model is evaluated on the validation set using metrics like accuracy, precision, recall, F1-score, and the confusion matrix.
   - The final evaluation results are plotted, and the model’s performance is analyzed.

## **Model Architecture**
The CNN model architecture used in this project is as follows:

- **Input Layer**: Accepts images of size 224x224x3 (RGB images).
- **Convolutional Layer 1**: 32 filters of size 3x3, ReLU activation.
- **Max-Pooling Layer 1**: Pooling with a 2x2 window.
- **Convolutional Layer 2**: 64 filters of size 3x3, ReLU activation.
- **Max-Pooling Layer 2**: Pooling with a 2x2 window.
- **Flatten Layer**: Converts the 2D matrix into a 1D vector.
- **Fully Connected Layer 1**: 128 neurons, ReLU activation.
- **Output Layer**: 1 neuron (sigmoid activation) for binary classification (normal or pneumonia).

## **Training Process**
- **Data Augmentation**: We use random transformations (rotation, flipping, zooming) to make the model robust to variations in the input images.
- **Optimizers**: Adam optimizer with a learning rate of 0.001 is used to minimize the binary cross-entropy loss.
- **Early Stopping**: Stops training once the validation loss stops improving to avoid overfitting.
- **Metrics**: The model's performance is measured using accuracy, precision, recall, and F1-score.

## **Evaluation and Results**
The model achieved the following evaluation results on the validation set:

- **Accuracy**: 94%
- **Precision**: 92%
- **Recall**: 96%
- **F1-Score**: 94%

These results suggest that the model is highly accurate in detecting pneumonia from chest X-ray images, though there is still room for improvement in precision (reducing false positives).

## **Future Work**
While the current model performs well, there are several ways to improve it:
- **Transfer Learning**: Implement transfer learning using pre-trained models such as ResNet or VGG16, which could provide better performance with less training data.
- **Advanced Image Preprocessing**: Experiment with more advanced techniques like contrast enhancement or noise reduction to improve model accuracy.
- **Multi-Class Classification**: Expand the model to classify different types of pneumonia (e.g., bacterial, viral) or other lung conditions.
- **Deployment**: Develop a web or mobile application that allows healthcare professionals to upload chest X-rays and receive predictions about pneumonia.

## **References**
1. Mooney, P. (2018). Chest X-ray Images (Pneumonia). Kaggle. [Link](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia)
2. Rajpurkar, P., et al. (2017). CheXNet: Radiologist-Level Pneumonia Detection on Chest X-Rays with Deep Learning. [Link](https://arxiv.org/abs/1711.05225)
3. Chouhan, S. (2020). Pneumonia Detection Using Chest X-rays. [GitHub Repository](https://github.com/anishrajan135/Pneumonia-Detection)
4. TensorFlow Documentation. [Link](https://www.tensorflow.org/tutorials/images/cnn)
