Overview
This project implements a Long-Term Recurrent Convolutional Network (LRCN) for Human Activity Recognition (HAR) using machine learning. The model is designed to classify various human activities based on video frames, extracting both spatial and temporal features from the input data. The LRCN architecture uses convolutional layers for feature extraction and LSTM layers for modeling temporal dependencies, making it suitable for video-based activity recognition.

Features
Spatial Feature Extraction: Convolutional layers (Conv2D) are used to extract spatial features from each video frame.
Temporal Sequence Modeling: LSTM layers capture the temporal dependencies between frames, allowing the model to learn the dynamics of the activities.
TimeDistributed Layer: Ensures that the same layer is applied independently to each frame in the video sequence.
Model Regularization: Dropout layers are added to prevent overfitting during training.
End-to-End Training: The model is trained end-to-end, learning both spatial and temporal features directly from the video data.

Dataset
This project can be applied to various human activity recognition datasets:


Example Activities:
Walking
Running
Sitting
Standing
Laying down

Requirements
Python 3.8+
TensorFlow (for model construction and training)
NumPy
Matplotlib
OpenCV (optional, for video frame extraction)
scikit-learn (for data preprocessing)
To install the required libraries, run the following command:

Model Architecture
The LRCN model consists of the following layers:

TimeDistributed Conv2D Layers: Apply convolution operations to each frame independently.
MaxPooling2D: Reduces spatial dimensions.
Dropout: Regularizes the model to prevent overfitting.
LSTM Layer: Models the temporal sequence of frames.
Dense Layer: Produces the final classification output.
