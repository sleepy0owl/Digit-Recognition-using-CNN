# Digit-Recognition-using-CNN
Digit recognition using MNIST data and Keras with Tensorflow backend.
* This kernel is for the Kaggle competition [Digit Recognizer](https://www.kaggle.com/c/digit-recognizer) .
* This competition uses MNIST dataset where each image is 28x28 pixels and there are 42000 images for training.
* Using CNN I have achived .99657 public score which is [top 10%](https://www.kaggle.com/sourav13) and my rank is 262nd.
# About Model 
## CNN Architecture
[Input] -->[Conv2D] -->[Conv2D] -->[MaxPool2D] -->[Conv2D] -->[Conv2D] -->[MaxPool2D] -->[Flatten] -->[Dense] -->[Dense] -->[ouput]
## Parameters
* 1st and 2nd Conv layers 40 filters, padding 'same', filter size 5x5.
* Maxpool size 2x2 and stride is pool size
* 3rd and 4th Conv layers 60 filters, padding 'same', filter size 3x3.
* 1st dense or fully connected layer has 300 units.
* Last dense layer has 10 unit beacuse there are 10 different classes.
## Activation
* For conv layers and dense layer1 **Relu** is used.
* For dense layer2 **SoftMax** is used.
## Optimizer
* Here I have used **Adam** optimizer with **LearningRate** *0.001*, **beta1** *0.9*, **beta2** *0.999*, **epsilon** *NONE*, **Decay** *0.0.
* I have used **Categorical Cross entropy** as loss function and **accuracy** as metric.
## Training the model
* I have split the entire training dataset to train and cross valodation set, where 99% of training data is used for training and 1% for cross validation.
* epochs 30 and batch size 84.
# Libraries used
**keras,pandas, numpy, matplotlib, seaborn**.
