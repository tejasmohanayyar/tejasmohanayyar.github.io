---
layout: post
title: Classification of Animals in the wild using CNN models and Tensorflow (Keras)
permalink: animals-classification-cnn

---

<img src="/images/Animals_classification/animals_trainset.png"> 

### Dataset used for the experiement

I have used the [African wildlife](https://www.kaggle.com/biancaferreira/african-wildlife) dataset for my experiment.

### Contents of this article:
* What are Convolutional Neural Networks
* Implementing 4 different CNN models on the mentioned dataset.
* Presenting comparative findings for the 4 implemented models.
* Conclusions

### What are Convolution Neural Networks?

* A Convolutional Neural Network is a type of artificial neural network that is primarily used for image recognition applications. It consists of multiple layers called perceptrons for learning features present in images with utmost detail. 

* "Convolution" here represents the understanding of features within an image. Extracting these features entails the entire process of convolution.

* To extract these features we use filters and mention the number of filters to be used (Kernels). 

* Pooling is another concept in CNN. It is used to reduce the number of features that we get after we have run our filters over the images. The filters cause us to get a large number of features compared to the image itself. So pooling is used to get a better generalized representation of the same. For example a 25x25 image might end up with 100x100 features due to the number of filters (kernels) and their shape. Pooling can reduce these features either using max pooling or mean pooling. I will not delve much into what pooling is.

* Padding is another CNN concept where we add zeros to the edges of an image. This is done for 2 reasons. To better read the edge features and to get similar output as the input image.

* Lastly the output of the CNN is flattened and sent into a fully connected layer. This is our Neural Network part of CNN. It will enable the machine to learn from the extracted features and create a generalized model. 

* To know more about Convolutional Neural Networks I would start from this [video](
https://youtu.be/aircAruvnKk).

### The CNN models timeline

### LeNet
<img src = "https://www.researchgate.net/profile/Sheraz_Khan8/publication/321586653/figure/fig4/AS:568546847014912@1512563539828/The-LeNet-5-Architecture-a-convolutional-neural-network.png">

* The LeNet architecture was invented in 1998 by Yann Lecun with the aim to be able to perform Optical Character Recognition (OCR). The architecture is very small and simple compared to other architectures. The image set consisted of images of numbers from 0-9 in black and white.

* It consists of 3 convolution layers and 3 pooling layers. After these layers the outputs are flattened and the data is sent into a Fully connected layer. The last dense layer of the Neural Network can be any activation function for predicting the output. 

* Across the entire network according to the paper published for LeNet, activation functions across all the layers were tanh. I have used the same activation function for this network. We have to remember that the commonly used activation functions used today were not there in 1998.

##### Implementation in your example and your findings
<img src="/images/Animals_classification/lenet_output.png"> 

* As can be observed from the above graph of accuracy, we can clearly see the slow learning rate that this model is displaying. There could be many reasons for this. The lack of depth of this network is one reason. Another reason could be the activation function tanh which has been used. However it does not have much of an impact since I have trained the same dataset and model with the relu activation function and there wasn't a significant impact.

* The validation accuracy also comes down slowly which shows a slow learning rate for this model.

##### Advantages

* This network was a good introduction into the world of neural networks and is really simple to understand. It works well for character recognition images.

##### Disadvantages

* This model was more specifcally built for a certain use case. While it was a major breakthrough in 1998, it does not do as well with color images. Most image recognition problems would require RGB images for better recognition.

* Since the model isn't very deep, it struggles to scan for all features thus producing poor performing models. If the Neural Network isn't fed with enough features from the training images then it would be difficult for the model to generalize and create an accurate model.

### AlexNet
* The AlexNet architecture was introduced in 2012 at the ImageNet Large Scale Visual Recognition Challenge. 
* It was designed by Alex Krizhevsky and published with Illya Sutskever and Krizhevsky's doctoral advisor Dr. Geoffrey Hinton.
* AlexNet consisted of 8 layers and used the ReLu activation function which was a major discovery in deep learning. 
* It was the first GPU based CNN model and was 4 times faster than previous models.


* Implementation in your example and your findings
<img src="/images/Animals_classification/alexnet_output.png">

##### Advantages

* AlexNet was the first major CNN model that used GPU's for training. This lead to faster training of models.
* AlexNet is a deeper architecture with 8 layers which means that is better able to extract features when compared to LeNet. It also worked well for the time with color images.
* The ReLu activation function used in this network has 2 advantages. It does not limit the output unlike other activation functions. This means there isn't too much loss of features.
* It negates the negative output of summation of gradients and not the dataset itself. This means that it will further improve model training speed since not all perceptrons are active.

##### Disadvantages


* Compared to models used further in this article, the depth of this model is very less and hence it struggles to learn features from image sets. 

* We can see that it takes more time to achieve higher accuracy results. **check**


##### VGG
* About VGG

* Implementation in your example and your findings
<img src="/images/Animals_classification/VGG_output.png">

* Advantages
* Disadvantages

***There is the Inception-V1 and Inception-V3 models that came in 2006 and 2008 as well but I have skipped those models from my experiment.**

##### ResNet
* About ResNet
* Implementation in your example and your findings
<img src="/images/Animals_classification/Resnet_Output.png">

* Advantages
* Disadvantages

### Presenting comparative findings for the 4 implemented models.

### Conclusions

I performed this experiment to get a better understanding of the different types of model and how do they practically impact training of image classification models. You can further explore this experiment on my colaboratory notebook [here](https://www.google.com). The images used are from [this kaggle competition](https://www.google.com). 

Thanks for reading!
