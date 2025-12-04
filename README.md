# Hand Gesture Detection

A deep learning project for detecting and classifying hand gestures using **MobileNetV2** and **Keras**.  
The model is trained on YOLO-format annotations (class_id, x_center, y_center, width, height) and outputs both the gesture class and the bounding box coordinates.

## Dataset
The project uses a **YOLO-style dataset** for training and evaluation.  
Each image has a corresponding `.txt` annotation file with the following format:
- (class_id x_center y_center width height)
- **class_id** → integer representing the gesture category
- **x_center, y_center** → normalized coordinates (0–1) of the bounding box center relative to image width and height
- **width, height** → normalized dimensions (0–1) of the bounding box relative to image size

## Features
- Preprocessing pipeline for YOLO-style datasets
- Multi-output model:  
  - **Classification head** → predicts gesture class  
  - **Regression head** → predicts bounding box (x_center, y_center, width, height)
- Callbacks for training stability:
  - `ModelCheckpoint` to save the best model
- Visualization utilities to draw predicted bounding boxes and labels on images

## Requirements
- Python 3.8+
- TensorFlow / Keras
- NumPy
- OpenCV
- scikit-learn
- Matplotlib

