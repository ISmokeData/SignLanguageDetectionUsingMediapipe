# Sign Language Detection using MediaPipe and Deep Learning

This project implements real-time detection of sign language gestures for common phrases such as "hello," "please," "thank you," "no," "yes," and "I love you (ily)." It leverages **MediaPipe** and **OpenCV** for gesture detection, with a deep learning model built using **TensorFlow**.

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Model Architecture](#model-architecture)
- [Dataset](#dataset)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Features
- Real-time detection of six common sign language gestures.
- Uses **MediaPipe** for hand and pose detection.
- Live camera feed processing using **OpenCV**.
- Gesture recognition using a deep learning model (LSTM + CNN).
- Trained using custom data for accurate prediction.

## Technologies Used
- **MediaPipe**: For hand, head, and body pose detection.
- **OpenCV**: For video capture and image processing.
- **TensorFlow**: For building and training the deep learning model.
- **NumPy**, **Matplotlib**: For data manipulation and visualization.
- **TensorBoard**: For tracking loss and accuracy metrics during training.

## Installation
1. Clone this repository:
    ```bash
    git clone https://github.com/ISMokeData/sign-language-detection.git
    ```
2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage
1. Ensure you have a webcam connected.
2. The camera will start capturing video, and the model will recognize hand gestures for the supported signs.

## Model Architecture
The model is a Sequential neural network, consisting of:
- **3 LSTM layers** for temporal sequence learning.
- **1 CNN layer** to extract spatial features.
- **2 fully connected layers** for classification.

The model is trained using the **Adam** optimizer, **categorical crossentropy** loss, and **categorical accuracy** metrics.

## Dataset
- Custom dataset collected using **MediaPipe**.
- Data includes hand, head, and pose positions for each of the six gestures.
- Labeled and pre-processed for model training.

## Results
The model was trained for 500 epochs, with optimal results achieved at **143 epochs**, resulting in high accuracy. Training metrics were tracked using **TensorBoard**.

## Contributing
Feel free to submit issues or pull requests if you want to contribute to this project. Please follow the guidelines in the CONTRIBUTING.md file.

## License
This project is licensed under the MIT License. See the LICENSE file for details.
