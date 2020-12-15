---
layout: post
title: Face Mask Detection TFOD and Faster-RCNN
permalink: mask-detection

---

<img src="images/mask detection/maskdetectiondemo.gif" width="auto" height="auto" />

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
|Number of images annotated|855 images|
|Number of classes|2 (mask and without_mask)|
|Model used from model zoo|faster_rcnn_inception_v2_coco|
|Annotation format| PASCAL VOC|
|GPU used| NVIDIA Quadrio P4000 (Paperspace)|
|Number of training steps| 10000|
|Training Time| approx. 20 mins|
|Cost for training|$0.17|
|FPS achieved| 7 fps (Depends on computation power)|
|Tensorflow version|1.14.0|

We do not have a requirements file since we are working from the TFOD git repo that contains all the libraries required for the project.

## About the project

Working:

* We must first perform all the steps like creating tfrecords, creating a labelmap.pbtxt with our class names, move around some files before we can send start the training process.
* I used WinSCP to transfer files to the paperspace VM for training in the cloud.
* Using a public IP I was able to connect to the paperspace VM terminal through PUTTY allowing me to write terminal commands from my local system remotely.
* Post training and getting the inference graph (which contains the frozen weights) from training in the cloud we add it to our local folder to make our predictions.
* TFOD comes with an Object Detection Tutorial.ipynb which we will modify based on our usecase.
* I have also written code for making predictions on live video which I have reffered from different sources like OpenCV and for the detection I have refered to code from an online course from iNeuron that I was pursuing.
* The video output is in the header of this post.
* We get the following image outputs when trying to make predictions on images.

|||
|---|---|
|<img src="images/mask detection/2.png" width="auto" height="auto" />|<img src="images/mask detection/6.png" width="auto" height="auto" />|
|<img src="images/mask detection/3.png" width="auto" height="auto" />|<img src="images/mask detection/5.png" width="auto" height="auto" />|



## Conclusion

This project allowed me to create something useful and at the same time learn how to use the TFOD API. An ideal scenario for this project would be to use it to keep track of people about whether they are following the rule of wearing a face mask. You could have a look at the [github repo for this project](https://github.com/tejasmohanayyar/Face-Mask-Detection-using-TFOD-Faster-RCNN/tree/main) which contains just the ipynb notebook to make predictions and also download the entire zip with the training images [here](https://drive.google.com/file/d/1yjapsHDAN6QLJ5-aKInD19X7EVslaxJn/view?usp=sharing).