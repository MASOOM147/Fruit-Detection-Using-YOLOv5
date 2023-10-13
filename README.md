# Fruit-Detection-Using-YOLOv5
This README file provides an overview and explanation of the code for Fruit Image Classification and YOLOv5 Training. The code's purpose is to prepare an image dataset for fruit classification and train a YOLOv5 object detection model.

## Table of Contents
- [Introduction](#introduction)
- [Dataset Preparation](#dataset-preparation)
- [YOLOv5 Setup](#yolov5-setup)
- [Training](#training)
- [Conclusion](#conclusion)

---

## Introduction

The code presented here is designed for fruit image classification and YOLOv5 object detection training. The process involves several steps, including dataset preparation, YOLOv5 setup, and model training. Below is a breakdown of each major step:

---

## Dataset Preparation

1. **Data Directory Setup**: The code starts by setting up the directory paths for the training and test datasets. It also defines the output directory where processed data and YOLOv5 configuration will be saved.

2. **Data Preprocessing**: Image files are converted to the JPEG format, and associated XML annotation files are copied to a specific directory for further processing.

3. **XML Parsing**: XML files containing object annotations are parsed to extract information such as object labels, image dimensions, and bounding box coordinates. This information is then organized into a structured DataFrame for further use.

4. **Label Mapping**: A label mapping is created to map fruit labels ('orange', 'apple', 'banana') to numerical class indices (0, 1, 2).

5. **Data Visualization**: A sample image from the dataset is displayed for visualization purposes.

6. **Data Splitting**: The dataset is split into training and validation sets using the `train_test_split` function from scikit-learn.

---

## YOLOv5 Setup

7. **Cloning YOLOv5 Repository**: The YOLOv5 repository is cloned from GitHub to set up the YOLOv5 framework for training.

8. **Environment Setup**: The required dependencies for YOLOv5 are installed using the provided requirements file.

9. **Directory Creation**: Directories for storing YOLOv5 training data, labels, and images are created.

10. **Data Copying**: Images are resized and copied into the YOLOv5 training directory for both training and validation sets.

---

## Training

11. **Data Transformation**: The bounding box coordinates are transformed to fit the YOLOv5 model input size. Any infinite or missing values are removed from the dataset.

12. **Training Configuration**: A YAML configuration file is created to specify training and validation data paths, the number of classes, and class names ('banana', 'apple', 'orange').

13. **Training**: YOLOv5 training is initiated using the `train.py` script with defined settings such as image size, number of epochs, batch size, and the path to the configuration file.

---

## Conclusion

This README provides an overview of the code for fruit image classification and YOLOv5 training. The code takes raw image and annotation data, preprocesses it, and prepares it for YOLOv5 object detection training. By following the steps outlined in this README, you can train a custom object detection model for fruit detection.

For more details on YOLOv5 and its training process, refer to the official YOLOv5 repository and documentation.

**Note**: This code provides a simplified overview of the process, and real-world applications may require additional steps and optimizations.
