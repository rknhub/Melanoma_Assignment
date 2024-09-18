# Melanoma Detection using Convolutional Neural Network
> To build a CNN based model which can accurately detect Melanoma, a type of skin cancer


## Table of Contents
* [General Info](#general-information)
* [Model Overview](#model-overview)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
- The aim of this project is to build a multiclass classification model for detecting Melanoma a type of skin cancer, using a custom convolutional neural network in TensorFlow.
- Background: Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution which can evaluate images and alert the dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis. 
- Business probem: To successfully build a classification model to classify the given data set to different classes of cancer such as Actinic keratosis, Basal cell carcinoma, Dermatofibroma, Melanoma, Nevus, Pigmented benign keratosis, Seborrheic keratosis, Squamous cell carcinoma, Vascular lesion
- Dataset: The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->
## Model Overview
- Model Follows three Convolutional layers with varying feature maps such as 32, 64 & 128.
- For all layers, kernel size is 3x3 and activation function is relu
- Convolutional Layers are sandwiched between a dropout layer of 30% followed by a max pooling of pool size 2x2.
- After the 3 sandwiched layers, another Dropout layer of 30% followed by a Dense layer with relu activation
- Another dropout layer is added before finally adding the final Dense layer with the softmax function
- For model training, data was passed in to the model with a batch size of 32
- 30 Epochs were done to reach the final accuracy. 


## Conclusions
- Model Performance- Training Accuracy: 88.51% - Training loss: 0.2956. Validation Accuracy: 81.96% - Validation loss: 0.6204
- Inorder to improve the model several measures were tested including Dropouts and Batch Normalization.
- Batch Normalization did not improve the validation accuracy (rather it slowed down the learning).
- Using Dropouts after each convolutional layer,and before & after the flattening of layers significantly improved both the training and validation accuracy.
- The loss also followed the same path of reducing the training and validation accuracy with dropouts.
- The model was tested with 50 epochs and the model started overfitting, but the validation accuracy was more or less the same, hence reverted back to the 30 epoch model.


<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- Python
- Tensorflow

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
Give credit here.
- Thanks to the Upgrad team for a well structured curriculam
- Thanks to all the mentors from recorded and live sessions.
- This project was part of assignment from the Deep Learning module from my Masters programme with LJMU


## Contact
Created by [@rknhub] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
