---
layout: post
title: Personal Protective Equipment Detection using TFOD and Faster-RCNN
permalink: ppe-detection

---

<img src="images/PPE detection/13.png" width="auto" height="auto" />

**What this post is going to cover:**

* What is TFOD
* About Faster-RCNN
* About the project
* Conclusion

## Introduction to TFOD

Tensorflow Object Detection is an Object Detection API created by google's Tensorflow using the tensorflow library and the Keras API. For this project I have used the faster-rcnn model pre-trained on the COCO dataset. This project is an example of transfer learning where we train our own model over the existing COCO model. This makes our model more accurate since the model has already learned vertical and horizontal features over the COCO dataset. It will be able to generalize in a much better manner.

## About Faster-RCNN

We are using faster-RCNN since it provides accurate results and is better than RCNN and fast-RCNN. Faster-RCNN uses the concept of region proposal networks instead of the selective search algorithm which was previously seen in RCNN and fast-rcnn. Rather than having a predefined number of bounding boxes, our RPN is a neural network that is able to learn the position of bounding boxes and identify objects within the box. It consists of a classifier using the softmax algorithm to predict the class and a regressor to determine the co-ordinates of the bounding boxes. RCNN used selective search and was hard coded to make 2000 bounding boxes while looking for classes. Faster RCNN used learning algorithms to get precise co-ordinates for bounding boxes. Since they were hard coded, and used more number of bounding boxes they were slower and took longer.

While faster-RCNN performs better but provides a very low FPS. The You Only Look Once (YOLO) algorithm improves on the FPS while maintaining Faster-RCNN level accuracy.

## Specfications of the project

|Parameter|Specification|
|---|---|
|Tool used for image annotation|Labelimg|
|Number of images annotated|600 images|
|Number of classes|4 (earmuff,helmet,mask,glasses)|
|Model used from model zoo|faster_rcnn_inception_v2_coco|
|Annotation format| PASCAL VOC|
|GPU used| NVIDIA Quadrio P4000 (Paperspace)|
|Number of training steps| 10000|
|Training Time| approx. 30 mins|
|Cost for training|$0.20|
|Tensorflow version|1.14.0|

We do not have a requirements file since we are working from the TFOD git repo that contains all the libraries required for the project.

## About the project

Working:

* Do annotations for all images for the respective classes using a tool like labelimg.
* Download the TFOD repo from [here](https://github.com/tensorflow/models/tree/v1.13.0) to get started with the project.
* We must first perform all the steps like creating tfrecords, creating a labelmap.pbtxt with our class names, move around some files before we can send start the training process.
* I used WinSCP to transfer files to the paperspace VM for training in the cloud.
* Using a public IP I was able to connect to the paperspace VM terminal through PUTTY allowing me to write terminal commands from my local system remotely.
* Post training and getting the inference graph (which contains the frozen weights) from training in the cloud we add it to our local folder to make our predictions.
* TFOD comes with an Object Detection Tutorial.ipynb which we will modify based on our usecase.
* We get the following image outputs when trying to make predictions on images.
* More number of images will give much better results but as can be seen in the below images the outputs are quite good for 700 images as input.

|||
|---|---|
|<img src="images/PPE detection/2.png" width="auto" height="auto" />|<img src="images/PPE detection/3.png" width="auto" height="auto" />|
|<img src="images/PPE detection/4.png" width="auto" height="auto" />|<img src="images/PPE detection/5.png" width="auto" height="auto" />|



## Conclusion

This project allowed me to create something useful and at the same time learn how to use the TFOD API. An ideal scenario for this project would be to use it to keep track of people about whether they are following the rule of wearing all the safety equipment required while working in the industry. I got the idea to do this project from an internship that I had done duing my Diploma at L&T Powai. You could have a look at the [github repo for this project](https://github.com/tejasmohanayyar/Personal-Protective-Equipment-Detection-using-TFOD) which contains just the ipynb notebook to make predictions and also download the entire zip with the training images [here](https://drive.google.com/file/d/1298qMacZm_QOeuTRmLlterE7G8TC0UAX/view).
