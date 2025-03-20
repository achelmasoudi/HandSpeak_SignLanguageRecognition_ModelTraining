<div align="center">
      <h1> 
            <img src="https://github.com/user-attachments/assets/777a991d-7eb5-4c4a-b25c-a7ec0e63d9c3" width="185px">
            <br/>
            HandSpeak - Sign Language Recognition ( Model Training )
            <br/> 
      </h1>
</div>

**HandSpeak** is a machine learning project designed to recognize American Sign Language (ASL) gestures representing letters A-Z and "space." This repository contains the model training code and resources, leveraging a pre-trained EfficientNetB0 model to classify hand signs from images.

<br/>

## Project Overview
- **Objective:** Train a model to classify 27 ASL signs (A-Z and space) from hand gesture images.
- **Dataset:** ASL Alphabet, containing images for 27 classes.
- **Model Performance:** Uses Mean Absolute Error (MAE) as the metric; specific accuracy/loss values depend on training results (tracked via validation MAE).
- **Technologies:** Python, TensorFlow, Keras, OpenCV, EfficientNetB0.

<br/>

## Model Details
- **Architecture:** Based on EfficientNetB0 (pre-trained), with added layers:
  - Global Average Pooling 2D.
  - Dropout (30%) to prevent overfitting.
  - Dense layer (1 neuron) for regression output.
- **Input:** 96x96 RGB images.
- **Training:** 50 epochs, batch size 32, Adam optimizer, MAE loss, ModelCheckpoint, ReduceLROnPlateau.
- **Output Format:** Converted to TensorFlow Lite (sign_lan.tflite) for mobile integration.

<br/>

## Android Integration
The trained model is integrated into a real-time Android app.
- ✅ **Check it out here :** [HandSpeak Android App](https://github.com/achelmasoudi/HandSpeak_App)

<br/>

## Visualizations
- **Class Distribution:** Bar chart of image counts per class (A-Z, space).
- **Training Metrics:** Plots for training/validation loss and MAE.
- **Confusion Matrix:** Visualizes model performance across classes.
