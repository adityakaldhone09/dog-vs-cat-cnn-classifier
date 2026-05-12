# dog-vs-cat-cnn-classifier

This model is a Convolutional Neural Network (CNN) classifier built to distinguish between images of dogs and cats. It was developed using TensorFlow and Keras and trained on the "salader/dogsvscats" dataset from Kaggle.

Dog vs. Cat CNN Classifier
A deep learning project that utilizes a multi-layer Convolutional Neural Network (CNN) to classify images as either a "dog" or a "cat."

Project Overview
The model processes color images of size 256x256 pixels. It includes standard CNN components like Convolutional layers, Batch Normalization to speed up training, MaxPooling for downsampling, and Dropout layers to prevent overfitting.

Model Architecture
The network follows a sequential architecture:

Convolutional Layers: 3 layers with 32, 64, and 128 filters respectively, all using 3×3 kernels and ReLU activation.

Normalization & Pooling: Each convolutional layer is followed by a BatchNormalization layer and a MaxPooling2D layer (2×2 pool size).

Dense Layers: After flattening the features, the data passes through two fully connected layers (128 units and 64 units) with Dropout (0.1).

Output Layer: A single unit with a Sigmoid activation function for binary classification.

Steps Initiated
The development process involves the following key stages as seen in the notebook:

Dataset Acquisition: Downloads the dataset using kagglehub and extracts the files into the environment.

Data Loading & Preprocessing:

Uses image_dataset_from_directory to load 20,000 training files and 5,000 test files.

Resizes all images to 256×256.

Normalization: Scales pixel values from [0, 255] to [0, 1] for better model convergence.

Model Training:

Optimizer: Adam optimizer.

Loss Function: Binary Crossentropy.

Epochs: Trained for 10 epochs.

Evaluation:

Plots training vs. validation accuracy.

Plots training vs. validation loss to check for overfitting.

Prediction: Includes a script to reshape and predict the class of a single test image.

Requirements
1.Python 3
2.TensorFlow / Keras
3.OpenCV (cv2)
4.Matplotlib
5.Kagglehub (for data download)
