## KittyOrDoggo
This repository contains:
Presentation:[Kitty Or Doggo? Presentation](https://docs.google.com/presentation/d/1AMoVtYK_Xoi3qsslMUUjs7qglIKG-jV50nWwnqvV0Ck/edit?usp=sharing)
Design Documentation:[Kitty Or Doggo? Project Report](https://docs.google.com/document/d/16USbMaZ3z7cXQ3zDwXxzpBge3Q9r8tU2Ul9E6j3cU0c/edit?usp=sharing)

Jin An | CS MS | Yale University
Tian Wang | CS MS | Yale University
Qingning Yao | CS MS | Yale University
Angel Zhang | CS MS | Yale University

## Project Introduction
## 1.1 Motivation and Background
The purpose of this project is to develop an image classifier to distinguish dogs and cat, which is the Dogs vs. Cats competition from Kaggle. Although it is easy for humans to differentiate dogs and cat, there is evidence indicating that dogs and cats are particularly difficult to tell apart automatically. Therefore, accomplishing this Kaggle competition would lead us a step closer to to solve the Completely Automated Public Turing test to tell Computers and Humans Apart (CAPTCHA) challenge. 

To address this problem, many groups have attempted to construct different neural networks and machine learning algorithms and achieved accuracies ranging from 56.9% to 92.9%. These previous implementations include color-feature-based classifiers, SVM classifiers based on color and texture features, and pre-trained classifier based on SIFT(Scale-Invariant Feature Transform) features[1].

## 1.2 Project Task Definitions
The goal of the project is to create an algorithm to classify whether an image contains a dog or a cat with an accuracy aiming at higher than 90%. Breaking down the project, there are two tasks to be completed, a learning task and a performance task using training dataset and test dataset, provided by Kaggle.

The learning task is to implement a classification model to learn the decision boundary for the training dataset. The flowgram would be: taking the training dataset as the input, extracting features from the input to obtain feature vector space, learning the model based on the feature space vector and real labels, and finally having the classification model with optimized parameters.

The performing task is to use the classification model to predict the labels of images as dogs and cats for the test dataset. Also, the classification accuracy will be evaluated as a percentage number. The flowgram would be: taking the test dataset as the input, extracting features from the input to obtain the feature vector space, using the trained classification model to generate predicted labels, and finally comparing the predictions with the real labels to have the classification accuracy.

## 1.3 Project Solutions
In this project, we have came up with several strategies to solve the Dogs vs Cats classification challenge. We implemented three different models to achieve higher performance. Starting with a simple convolutional neural network architecture with five layers, we implemented a training and testing program to obtain a baseline performance, from there, we fine tuned parameters--including learning rate, filter sizes, stride, dropout regularization rate, etc--to optimize resulting accuracies. Building on top of this simple convolutional neural network, we further expanded the network to be deeper, meaning more convolutional layers and pooling layers. However, as we found a bottleneck in designing a convolutional neural network through stacking layers, we approached a different stratege. Considering the comparatively small-size dataset, we utilized transfer learning approach by adopting the pre-trained VGG16 network model and a two-step fine-tuning scheme to enhance the performance towards our goals.
