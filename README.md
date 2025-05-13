Gun Threat Detection Project
============================

This repository contains two main Jupyter notebooks:

1. Gun_Detector.ipynb
----------------------
This notebook handles:
- Data preprocessing
- Model training
- Model saving

It trains a machine learning/deep learning model to detect the presence of a gun in an image. The final trained model is saved and used in the next step.

2. Landmarks_detection.ipynb
----------------------------
This notebook uses the MediaPipe library to:
- Detect human hand landmarks in real-time.
- Specifically track the wrists and middle fingers.
- Calculate the distance between the wrist and middle finger to determine the hand's orientation and stability.
- Capture two images (whose size depend upon the distance between the wrist and middle finger landmards) of the hands based on landmark positions.

These images are then passed to the trained model from the `Gun_Detector.ipynb` notebook to:
- Predict whether a gun is present in either hand.

This setup allows real-time detection of gun threats based on hand landmarks and a trained classification model.

Requirements:
-------------
- Python
- OpenCV
- MediaPipe
- TensorFlow or PyTorch (depending on the model framework used)
- NumPy
- Jupyter Notebook

Note:
-----
The `data.zip` file and other large datasets/models may not be included in the repository due to size restrictions. Please ensure all dependencies and trained models are available before running the notebooks.
