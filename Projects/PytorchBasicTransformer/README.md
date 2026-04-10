# PytorchBasicTransformer

This project is a small Vision Transformer-style image classifier built in PyTorch for CIFAR-10.

## What This Project Covers

- Loading CIFAR-10 with separate training and evaluation transforms
- Splitting the training set into train and validation subsets
- Converting images into patch embeddings
- Adding learnable positional embeddings
- Passing patch tokens through stacked transformer encoder layers
- Pooling token outputs into a single image representation for classification
- Training on GPU when CUDA is available

## Current Model

The notebook in this folder defines a compact ViT-style model with:

- patch embedding through a convolutional projection
- learnable positional embeddings
- transformer encoder blocks with multi-head self-attention
- layer normalization
- mean pooling across patch tokens
- a linear classifier head

The training loop includes validation tracking and saves the best-performing model state before final test evaluation.

## Main File

- `model.ipynb`: notebook containing data preparation, model definition, training, validation, and final test evaluation

## Goal

The goal of this folder is to build intuition for how transformer-based vision models work in practice and to compare that workflow against the CNN baseline in the neighboring project.
