# **MAGANA - CSS182-4 AM4 Group 25 - Final Project**
This repository contains the files for my Final Project in Data Science 4 (CSS182-4) course.
<br><br>

## RF-DETR for Object Detection
This project explores the RF-DETR (Refined-Feature DETR) model for object detection. It involves building and evaluating an object detection model in Google Colab using a preprocessed and augmented dataset from Roboflow, visualizing predictions, and discussing the findings.
<br><br>
**Google Colab Notebook:** https://colab.research.google.com/drive/1wgboWolFmOxkSvQkdGITHxwJ9j5IiCY6?usp=sharing <br>
**Roboflow Dataset:** https://universe.roboflow.com/data-science-gubxu/plastic-o1ufz-zqhko 
<br><br>

## Setup and Implementation
Option 1: Clone the repository using 'git clone' command -> _git clone <repository_url>_ <br>
Option 2: Copy the .ipynb from the Google Colab notebook link <br>
Option 3: Download the .ipynb notebook
- After download, open the .ipynb notebook using Google Colab
- Make sure that the runtime is connected to a T4 GPU or higher
- Run each cell accordingly
<br>

## Results
The RF-DETR model was trained over 10 epochs on the preprocessed and augmented dataset. Evaluation metrics showed an improving trend across training loss and performance metrics. The training loss decreased consistently, while validation loss plateaued, suggesting mild overfitting. The Average Precision @0.50 peaked at 0.52 for the model, while the mean Average Precision across IoU thresholds reached approximately 0.27. Average Recall hovered around 0.60 - 0.65, indicating moderate detection completeness. Inference results on sample test images show the model accurately identifying and labeling plastic, metal, and paper objects, though some labels exhibit low confidence.

Considering the training hyperparameters, the RF-DETR showed good performance. However, False Positive and False Negative detections are still made particularly for objects that are not common types of the classes. These errors were likely due to class imbalance and visual similarity between waste types under varied lighting and background conditions as well as little training and lack of further hyperparameter tuning. The validation loss curve’s flat trajectory despite falling training loss suggests that generalization remains limited, and further hyperparameter tuning or more robust augmentations may be necessary.
