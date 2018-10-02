# Devanagari-Classifier-using-keras
Devanagari classification using Deep Learning with CNNs 

## Introduction:

This a Deep Neural Network I developed to classify devanagari numerals from 0 to 9 and consonants from 'ka' to 'gya'.The Dataset consisted of images of 32*32 pixels and 46 characters in total. The optimal accuracy obtained from the training set was 99.22% with loss(COST) of 0.0242 and 98.39% accuracy with loss of 0.0785 from the validation set. The source code is available on Github (under GPLv3 license), and the dataset is available on Kaggle. 

## Devanagari Script:

The Nāgarī or Devanāgarī alphabet developed from eastern variants of the Gupta script called Nāgarī, which first emerged during the 8th century.
The name Devanāgarī is made up of two Sanskrit words: deva, which means god, brahman or celestial, and nāgarī, which means city. The name is variously translated as "script of the city", "heavenly/sacred script of the city" or "script of the city of the Gods or priests".

## Deep learning:

Deep learning (also known as deep structured learning or hierarchical learning) is part of a broader family of machine learning methods based on learning data representations, as opposed to task-specific algorithms. Deep learning models are vaguely inspired by information processing and communication patterns in biological nervous systems yet have various differences from the structural and functional properties of biological brains (especially human brain).

## Project Description:

The following steps were taken to implement this model
### 1. Importing Dependencies
Libraries such as numpy for numeric computation, matplotlib for plotting, keras for creating a sequential deep network, os to manipulate directories to import dataset, cv2 to read the images are imported.
### 2. Loading Data
Data is loaded into train and test sets using cv2 module and os module. The data is then stored in the form of lists along with the labels in y_train and y_test. Data is shuffled before converting to a list to speed up learning. The list is then converted to a nparray using numpy module. Using pickle module we save and load the data for fast fetching of data.
### 3. Preprocesssing
The train and test data are normalized and the labels are given respective categories based on the number of classes which in this case is 46.
### 4. Creating Sequential Model
A Sequential Deep Neural net is formed by connecting two Conv2d layers with 32 and 64 kernels respectively with max pooling layers sandwitched between them to simplify the model or reduce the parameters. They are further connected to batch normalization to reduce covariate shifts layer and a flatten layer to flatten all the inputs to vectorize the input. This network is passed through a dense layer with 128 neurons followed by a dropout layer with dropout rate = 0.25 to overcome overfitting. All the layers consists of relu activation except the final layer. The output layer is connected to this network with softmax as its activation function and 46 output nodes. 

## CONCLUSION:

After training the dataset for 20 epochs with batch size = 32 we get 99.22% training accuracy and 98.39% validation accuracy. Learning rate I used here was 0.1. The tensorboard results show that the model is not overfitting as the natures of the curves of accuracy and losses for training and validation data are similar.

### REFERENCES:

www.deeplearning.ai

wikipedia

Michael Nielson book on www.neuralnetworksanddeeplearning.com

Jon Krohn Lectures on deep learning

### Contact:

ssiddharth080@gmail.com

