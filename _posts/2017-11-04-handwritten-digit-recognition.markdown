---
title: "Handwritten digit recognition"
layout: post
date: 2017-11-04
tag:
- ImageClassification
- DigitRecognition
- MachineLearning
image: https://raw.githubusercontent.com/amansingh9097/handwrittern-digit-recognition/master/mnist.png
headerImage: true
projects: true
description: "Teaching machines to recognize hand written digits."
category: machine-learning
author: Aman Singh
---

Teaching machines to recognize hand written digits.

#### Data Description:
MNIST ("Modified National Institute of Standards and Technology") is the de facto “hello world” dataset of computer vision. Since its release in 1999, this classic dataset of handwritten images has served as the basis for benchmarking classification algorithms. As new machine learning techniques emerge, MNIST remains a reliable resource for researchers and learners alike.

The goal is to correctly identify digits from a dataset of tens of thousands of handwritten images. 

#### Introduction:
This is a 5 layered Convolutional Neural Network trained on MNIST dataset. I've used **Keras** framework for building the Neural Net architecture. I was able to achieve a public score of 99.5% categorization accuracy on the unseen data with a rank of 426/2255 which in turn is among **Top 6%** in the Public Leaderboard. [**Update:** the rank is from date Jun 19, 2017 21:33, current rank may differ]

**Number of training examples per digit:**<br>
<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/digit-recognizer/mnist_distribution.PNG">

**CNN Model Architecture**<br>
```
Model: "sequential_1"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
conv2d_1 (Conv2D)            (None, 28, 28, 32)        832       
_________________________________________________________________
conv2d_2 (Conv2D)            (None, 28, 28, 32)        25632     
_________________________________________________________________
max_pooling2d_1 (MaxPooling2 (None, 14, 14, 32)        0         
_________________________________________________________________
dropout_1 (Dropout)          (None, 14, 14, 32)        0         
_________________________________________________________________
conv2d_3 (Conv2D)            (None, 14, 14, 64)        18496     
_________________________________________________________________
conv2d_4 (Conv2D)            (None, 14, 14, 64)        36928     
_________________________________________________________________
max_pooling2d_2 (MaxPooling2 (None, 7, 7, 64)          0         
_________________________________________________________________
dropout_2 (Dropout)          (None, 7, 7, 64)          0         
_________________________________________________________________
flatten_1 (Flatten)          (None, 3136)              0         
_________________________________________________________________
dense_1 (Dense)              (None, 256)               803072    
_________________________________________________________________
dropout_3 (Dropout)          (None, 256)               0         
_________________________________________________________________
dense_2 (Dense)              (None, 10)                2570      
=================================================================
Total params: 887,530
Trainable params: 887,530
Non-trainable params: 0
_________________________________________________________________
```

**Training loss vs Validation loss & Training accuracy vs Validation accuracy**<br>
<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/digit-recognizer/accuracy_loss.PNG">

**Confusion Matrix**<br>
<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/digit-recognizer/conf_mat.PNG">

**Some examples**<br>
<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/digit-recognizer/examples.PNG">

**Data Source:** [Kaggle](https://www.kaggle.com/c/digit-recognizer)

Check out the whole project on [GitHub](https://nbviewer.jupyter.org/github/amansingh9097/handwrittern-digit-recognition/blob/master/mnist-classifier.ipynb)

--- 

If you liked this project, please consider buying me a coffee<br>
<style>.bmc-button img{height: 34px !important;width: 35px !important;margin-bottom: 1px !important;box-shadow: none !important;border: none !important;vertical-align: middle !important;}.bmc-button{padding: 7px 10px 7px 10px !important;line-height: 35px !important;height:51px !important;min-width:217px !important;text-decoration: none !important;display:inline-flex !important;color:#ffffff !important;background-color:#FF813F !important;border-radius: 5px !important;border: 1px solid transparent !important;padding: 7px 10px 7px 10px !important;font-size: 28px !important;letter-spacing:0.6px !important;box-shadow: 0px 1px 2px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;margin: 0 auto !important;font-family:'Cookie', cursive !important;-webkit-box-sizing: border-box !important;box-sizing: border-box !important;-o-transition: 0.3s all linear !important;-webkit-transition: 0.3s all linear !important;-moz-transition: 0.3s all linear !important;-ms-transition: 0.3s all linear !important;transition: 0.3s all linear !important;}.bmc-button:hover, .bmc-button:active, .bmc-button:focus {-webkit-box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;text-decoration: none !important;box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;opacity: 0.85 !important;color:#ffffff !important;}</style><link href="https://fonts.googleapis.com/css?family=Cookie" rel="stylesheet"><a class="bmc-button" target="_blank" href="https://www.buymeacoffee.com/amansingh"><img src="https://cdn.buymeacoffee.com/buttons/bmc-new-btn-logo.svg" alt="Buy me a coffee"><span style="margin-left:15px;font-size:28px !important;">Buy me a coffee</span></a>