# Sign Language Detection using LSTM and Mediapipe

This repository contains code for a Sign Lnaguage Recognition system that uses the Mediapipe library for pose estimation and hand tracking, as well as LSTM (Long Short-Term Memory) for sequence classification. The system is designed to recognize and classify hand gestures from webcam video input.

## 1. Business Understanding
The Gesture Recognition system is developed to detect and classify hand gestures in real time. It can be used in various applications, such as sign language recognition, human-computer interaction, or gesture-based control systems. By understanding and recognizing different hand gestures, the system can enable more natural and intuitive interactions with computers and devices.


## 2. Results
The system achieves gesture recognition in real-time from webcam input. It can detect and classify hand gestures with a high degree of accuracy, providing the recognized gestures as output. The recognized gestures are displayed on the screen in real-time, allowing users to interact with the system by performing different hand gestures.


## 3. Technologies used.

#### a. Programing Languages
1. Python

#### b. Libraries 
1. OpenCV: For capturing webcam feed and image processing.
2. Matplotlib: For visualizing image data.
3. NumPy: For array manipulation and data handling.
4. Mediapipe: For pose estimation and hand tracking.
5. TensorFlow: For creating and training the LSTM model.


## 4. Approach

The project follows these main steps:

1. Data Collection: The system captures video frames from the webcam and uses the Mediapipe library to detect the pose and landmarks of the face, hands, and body.

2. Landmark Extraction: The extracted landmarks are processed to extract keypoints for the face, pose, and both hands. The keypoints are then concatenated to form a feature vector.

3. Data Preprocessing: The collected data is split into sequences, each containing a fixed number of frames (sequence_length) for each gesture (action).

4. Model Training: An LSTM model is created using TensorFlow. The LSTM layers are designed to learn the temporal patterns in the input sequences and classify the gestures accordingly. The model is trained using the training data.

5. Gesture Recognition: During real-time gesture recognition, the system continuously captures frames, extracts keypoints, and forms sequences of keypoints. These sequences are fed into the trained LSTM model to predict the recognized gestures.

6. Real-Time Visualization: The recognized gestures are displayed on the screen in real-time. If a gesture is held for a certain threshold of confidence, it is considered a recognized gesture and displayed as part of a sentence. The last five recognized gestures are displayed as a sentence.

The system can be extended to recognize more gestures by adding new actions to the "actions" array in the code.

