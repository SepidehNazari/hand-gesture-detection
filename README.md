# Hand Gesture Detection

A deep learning project for detecting and classifying hand gestures using **MobileNetV2** and **Keras**.  
The model is trained on YOLO-format annotations (class_id, x_center, y_center, width, height) and outputs both the gesture class and the bounding box coordinates.

## Features
- Preprocessing pipeline for YOLO-style datasets
- Multi-output model:  
  - **Classification head** → predicts gesture class  
  - **Regression head** → predicts bounding box (x_center, y_center, width, height)
- Callbacks for training stability:
  - `ModelCheckpoint` to save the best model
  - `EarlyStopping` to prevent overfitting
- Visualization utilities to draw predicted bounding boxes and labels on images

## Project Structure
