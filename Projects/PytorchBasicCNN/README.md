# PytorchBasicCNN

This project is a beginner-friendly convolutional neural network baseline built in PyTorch for handwritten digit classification on MNIST.

## What This Project Covers

- Loading and normalizing MNIST with `torchvision`
- Splitting the training data into training and validation subsets
- Building a simple CNN with convolution, ReLU, max pooling, flattening, and linear layers
- Training with cross-entropy loss and Adam
- Tracking validation performance before running a final test evaluation

## Current Model

The notebook in this folder defines a small CNN with:

- two convolutional blocks
- max pooling after each block
- a flattened feature vector
- a two-layer classifier head

This project acts as a baseline computer vision pipeline and a reference point for later transformer-based experiments.

## Main File

- `model.ipynb`: notebook containing data loading, model definition, training, validation, and test evaluation

## Goal

The goal of this folder is to provide a simple, interpretable CNN training workflow that can be compared against more advanced vision architectures later in the repository.
