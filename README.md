# PRODIGY_ML_04
# Gesture Recognition Program Read Me

This README file provides an overview of the Gesture Recognition program, detailing its purpose, functionality, and steps for usage.

## Program Description

The Gesture Recognition program is designed to train a Convolutional Neural Network (CNN) model to recognize hand gestures from images. It takes as input a dataset of images where each image corresponds to a hand gesture and classifies the gestures into different categories. The program preprocesses the data, trains the model, and provides information about the loss and accuracy.

## Program Components

The program is divided into several key components:

1. **Data Loading and Preprocessing:** The program loads a dataset of hand gesture images and performs the following preprocessing steps:
   - Reads image files using OpenCV (cv2).
   - Resizes images to a uniform size of 64x64 pixels.
   - Normalizes pixel values to the range [0, 1].

2. **Label Encoding and One-Hot Encoding:** The program encodes the labels (gesture names) to numeric values using LabelEncoder. It then performs one-hot encoding to convert the numeric labels into a binary matrix.

3. **CNN Model Definition:** A Convolutional Neural Network (CNN) model is defined with the following architecture:
   - Input layer with a shape of (64, 64, 3), as the images are 64x64 pixels with 3 color channels.
   - Convolutional layers with activation functions.
   - Max-pooling layers.
   - A Flatten layer to prepare the data for fully connected layers.
   - Fully connected layers with ReLU activation functions.
   - Output layer with softmax activation for multi-class classification.

4. **Model Compilation:** The program compiles the model using the Adam optimizer and categorical cross-entropy loss. It also tracks accuracy as a metric.

5. **Model Training:** The model is trained using the training data for a specified number of epochs and with a specified batch size. The training process is monitored, and information about loss and accuracy is displayed.

## Usage

To use the Gesture Recognition program, follow these steps:

1. Ensure you have the necessary libraries installed, including OpenCV (cv2) and TensorFlow/Keras.

2. Organize your dataset in a folder structure with subdirectories, where each subdirectory represents a subject (e.g., individual person), and within each subject's folder, there are subdirectories for different gestures, each containing the gesture images.

3. Update the `Datasetpath` variable in the code to point to the root directory of your dataset.

4. Run the program. It will load, preprocess, and train the model.

5. After training, you will see information about the loss and accuracy, as provided in the example comment: `Loss is 'loss' and accuracy is 'accuracy`.

6. You can then use the trained model for gesture recognition tasks.

Feel free to customize the code and parameters to suit your specific dataset and requirements.

Happy gesture recognition! 🤖🖐✌
