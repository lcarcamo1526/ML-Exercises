# Introduction to Deep Learning with Google Colab and tensorFlow

We'll try to train our first neural network using only the basic foundations, the main goal here is make our neural network guess what formula we used to convert a temperature, where the approximate formula is:

Of course, it would be simple enough to create a conventional Python function that directly performs this calculation, but that wouldn't be machine learning.

![](https://video.udacity-data.com/topher/2019/March/5c7f0af9_tensorflow-l2f1/tensorflow-l2f1.png)


## What are we going to learn?

* What is a Dense Neural Network?
* How can we train our model?
* What is a Layer?
* What is the Weight of a NN?
* What is  ADAM?
* What is a Loss function?

![](https://video.udacity-data.com/topher/2019/March/5c7f0af9_tensorflow-l2f1/tensorflow-l2f1.png)


By now you should know what the following terms are:

  1. Feature: The input(s) to our model
  1. Examples: An input/output pair used for training
  1. Model: The representation of your neural network
  1. Labels: The output of the model
  1. Layer: A collection of nodes connected together within a neural network.
  1. Dense and Fully Connected (FC): Each node in one layer is connected to each node in the previous layer.
  1. Weights and biases: The internal variables of model
  1. Loss: The discrepancy between the desired output and the actual output
  1. MSE: Mean squared error, a type of loss function that counts a small number of large discrepancies as worse than a large number of small ones.
   1. Gradient Descent: An algorithm that changes the internal variables a bit at a time to gradually reduce the loss function.
   1. Learning rate: The “step size” for loss improvement during gradient descent.
    
