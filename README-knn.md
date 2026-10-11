# Handwritten-Digit Classification Using KNN

## Objective

Implement a K-nearest neighbors classifier using NumPy and study how the number of neighbors affects handwritten-digit classification.

## Dataset Preparation

The notebook loads MNIST using TensorFlow/Keras.

It combines the original training and test sets, normalizes pixel values to the range 0–1, and reshapes each 28×28 image into a vector of 784 features.

The combined dataset is shuffled with a fixed random seed and divided into a new 70% training split and 30% evaluation split.

## Classification Method

For each evaluation image:

1. Calculate squared Euclidean distances to the training images.
2. Select the nearest neighbors.
3. Predict the digit using majority voting among their labels.

Distance calculations are processed in batches. The nearest neighbors are reused to evaluate odd K values from 1 to 19.

## Evaluation

The notebook prints classification accuracy for each K, plots accuracy against K, and identifies the highest-scoring value.

The saved notebook output reports approximately 97.20% accuracy for K = 3 on its evaluation split. This split is also used to select K; it is not a separate final test set.

## Run

Open [knn_digit_classification.ipynb](knn_digit_classification.ipynb) in Google Colab and run the cell.

Dependencies: NumPy, Matplotlib, and TensorFlow.

MNIST is downloaded automatically. Evaluating all distances can take substantial computation time.
