# Abstract
This report discusses the application of deep learning models, YOLOv8 and
Faster R-CNN, for the task of airplane detection in aerial images. Both models
were trained and evaluated on a custom dataset, and their performance is compared
in terms of precision, recall, and mAP (mean Average Precision).

# 1. Introduction
The task of airplane detection plays a crucial role in surveillance, aviation, and geospatial
applications. In this project, we aim to evaluate the performance of two state-of-the-art
object detection models: YOLOv8 and Faster R-CNN. The motivation behind this com-
parison is to assess the strengths and weaknesses of these models for real-time detection
and accuracy in identifying airplanes in aerial imagery.

# 2. Problem Formulation
We treat the airplane detection task as an object detection problem, where the goal is to
identify and localize airplanes in images using bounding boxes. The dataset used in this
study contains aerial images annotated with bounding boxes around the airplanes.
The evaluation metrics used to assess model performance include:
• Precision
• Recall
• mAP50 (mean Average Precision at IoU threshold 0.5)
• mAP50-95 (mean Average Precision averaged over multiple IoU thresholds)

# 3. Methodology
## 3.1 Dataset
The dataset used for training and testing consists of aerial images with annotations in
YOLO format. The datatset was taken from the research article ”A benchmark dataset
for deep learning-based airplane detection: HRPlanes (https://dergipark.org.tr/en/pub/ijeg/arti
The dataset is split into training, validation, and test sets, with the images containing
airplanes labeled using bounding boxes.

## 3.2 Preprocessing and Augmentation
The images were resized to a fixed dimension, and basic augmentations such as flipping
and scaling were applied to improve model robustness. The training data was normalized,
and random crops were applied to simulate different detection scenarios.

## 3.3 Models
We compared the following models:
• YOLOv8: A modern one-stage detector that is known for its real-time performance.
• Faster R-CNN: A two-stage detector that is generally more accurate but slower.

## 3.4 Evaluation Metrics
We used precision, recall, and mAP as the primary evaluation metrics. The mAP scores
were calculated using the COCO evaluation metrics at various IoU thresholds
