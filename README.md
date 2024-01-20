# Face-Mask-Detection
The Objective of the project was to develop an algorithm using Convolutional Neural Network (CNN Model) for Facemask detection.
Convolutional Neural Network (CNN) for Face Mask Detection
This script defines and trains a CNN model to detect whether a person in an image is wearing a face mask or not. The model is trained on a dataset consisting of images with and without face masks.

Model Architecture:

The CNN model is created using the Sequential API from Keras.
The first layer is a 2D convolutional layer (Conv2D) with 32 filters, a kernel size of 3x3, ReLU activation function, and input shape of (64, 64, 3) representing the image dimensions (64x64 pixels with 3 color channels).
After the convolutional layer, a MaxPooling layer (MaxPool2D) with a pool size of 2x2 and strides of 2 is added to down-sample the spatial dimensions.
The same structure is repeated with another convolutional layer and max pooling layer.
A Flatten layer is added to convert the 2D feature maps to a 1D vector.
Two fully connected (Dense) layers follow, with 128 units and ReLU activation in the first layer, and a single unit with a sigmoid activation in the output layer for binary classification (mask or no mask).
Compilation and Training:

The model is compiled using the Adam optimizer and binary crossentropy loss function, which is suitable for binary classification problems.
The training data (training_set) and validation data (test_set) are used to train the model for 3 epochs.
Prediction:

After training, an image (check_4.jpg) is loaded for testing using the Keras image module. The image is resized to the input size expected by the model (64x64 pixels).
The image is converted to a NumPy array and expanded to include an additional dimension, making it compatible with the model.
The trained CNN is then used to predict whether the person in the image is wearing a mask or not.
The result is checked, and based on the prediction, the variable prediction is assigned either 'With Mask' or 'Without Mask'.
Class Indices:

The script prints the class indices from the training set, which can be useful for mapping the model's binary output to the corresponding classes ('With Mask' and 'Without Mask').
This script serves as the core of a face mask detection system and can be integrated into applications for real-time or batch processing of images to identify individuals wearing face masks.
