# Neural Network from Scratch (NumPy)
  
  I succesfully implemented Neural Network from Scratch using only NumPy.
  NumPy was used only for matrix manipulations and some computations, all actual network's logic was built using plain python. 
  The goal of the project was to deeply understand how neural networks work under the hood, and I actually understood a concept
  of back propagation with it.

## Overview

* Built a neural network from the scratch
* Implemented a custom Scalar class with automatic differentiation
* Implemented forward and backward propagation manually
* Focused on regression problems
* Used Mean Squared Error (MSE) as the loss function
* Implemented common activation functions:
  * Linear
  * ReLU
  * Softplus
  * Tanh
* Trained the model using gradient descent and mini-batches
* Compared model's predictions with official tensorflow.keras.Sequential model

## Dataset & Comparison

  The model was trained on a car sales price dataset from Kaggle:
  https://www.kaggle.com/datasets/yashpaloswal/ann-car-sales-price-prediction

  To make sure my model actually works, I decided to compare it with official tensorflow.keras model using same data and parameters

  I used MSE metric for loss function and used it as metric of accuracy, the lower the loss - the better the model is :D.
  
  Last losses:
  * Custom Model: 0.020
  * Keras Model: 0.0256

  The results are very close, which shows that the custom neural network works correctly for regression tasks.

## Key Takeaways

  * The project helped me fully understand how backpropagation works
  * Every part of the network is transparent and debuggable
  * The implementation is flexible and can be extended with:
    * more layers
    * new activation functions
    * additional metrics
    * different optimizers
    * callbacks and regularization

## Purpose
  
  This project is mainly educational, but it also demonstrates that a well-implemented neural network from scratch can perform competitively on real datasets.
