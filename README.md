# Neural Network from Scratch (NumPy)
  
  I succesfully implemented `Neural Network` from Scratch using only __NumPy__.
  __NumPy__ was used only for matrix manipulations and some computations, all actual network's logic was built using __plain python__. 
  The goal of the project was to deeply understand how neural networks work under the hood, and I understood a concept
  of _back propagation_ with it.

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
* Compared how training went for both models with loss curves.
* Compared MAE on test data for both models.

## Dataset & Comparison

  The model was trained on a car sales price dataset from Kaggle:
  https://www.kaggle.com/datasets/yashpaloswal/ann-car-sales-price-prediction

  To make sure my model actually works, I decided to compare it with official `tensorflow.keras` model using same data and parameters

  I used MSE metric for loss function and used MAE as metric of accuracy on test data.
  
  MAEs for both models on test data:
  - **Custom Neural Network MAE:** 0.2352
  - **Keras Neural Network MAE:** 0.1526

  Real error value on average for both models:
  - **Custom Neural Network MAE on the original price scale:** $18,814.24
  - **Keras Neural Network MAE on the original price scale:** $12,206.21

  The custom model produced a higher error on unseen data. This suggests that the custom model has higher variance and does not generalise as well as the Keras implementation.

  The result does not prove that the custom network is ready for real price prediction. It shows that the implementation can learn a regression task, while also showing where it needs improvement.


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
