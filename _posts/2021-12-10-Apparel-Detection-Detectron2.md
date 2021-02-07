---
layout: post
title: Apparel Detection using Facebook's Detectron 2 framework
permalink: apparel-detection-detectron2

---

<img src="images/Apparel Detection Detectron2/7.png" width="auto" height="auto" />

**What this post is going to cover:**

* What is Detectron2
* About Masked-RCNN
* About the project
* Conclusion

## Introduction to Detectron2

Detectron 2 is an image detection API built by Facebook over the mask-RCNN model. The idea is to detect a mask over a class rather than just a bounding box as is done with TFOD. 

## About Masked-RCNN

Masked-RCNN


## Specfications of the project

|Parameter|Specification|
|---|---|
|Tool used for image annotation|Labelme|
|Number of images annotated|50 for each class|
|Number of classes|4 (T-shirt,Watch,glasses,Jeans)|
|Model used from model zoo (COCO instance segmentation)|mask_rcnn_R_50_FPN_3x|
|Annotation format|PASCAL VOC|
|GPU used| NVIDIA P100 (Google Colab)|
|Number of training steps| 1000|
|Training Time| approx. 30 mins|
|Cost for training|Free|
|Pytorch version|1.15|

## About the project

Working:

* Do annotations for all images for the respective classes using a tool like labelme.
* Convert the annotations into one json file. Can be done with labelme2coco library. I personally used code that was provided to us as part of my Computer Vision course from iNeuron called [labelme2COCO.py](https://github.com/tejasmohanayyar/Apparel-Detection-using-Detectron2-Pytorch/blob/main/Apparel_Detection_detectron2/labelme2coco.py).
* Images and 1 json file should be added and zipped into a folder and uploaded to colab. The colab noteboook is available [here](https://github.com/tejasmohanayyar/Apparel-Detection-using-Detectron2-Pytorch/tree/main/Apparel_Detection_detectron2).
* We load the weights within the colab notebook and make inferences immediately.
* While this model gives us amazing results in terms of detection, the model size is 335 MB!
* It is not feasable to use this detectron model in a realtime application.
* I have been looking and trying to understand the concept of quantization and how I can make this model smaller.
* Quantization is a process where all the float weights are converted into int. This drastically reduces the size of the model and improves speed at the cost of accuracy.

|||
|---|---|
|<img src="images/Apparel Detection Detectron2/1.png" width="auto" height="auto" />|<img src="images/Apparel Detection Detectron2/2.png" width="auto" height="auto" />|
|<img src="images/Apparel Detection Detectron2/3.png" width="auto" height="auto" />|<img src="images/Apparel Detection Detectron2/4.png" width="auto" height="auto" />|



## Conclusion

I am stillvery new to the field of computer vision and am trying to learn new things and frameworks. As I learn something new I am trying to do a project to get some practical exposure. You can have a look at the entire project [here](https://github.com/tejasmohanayyar/Apparel-Detection-using-Detectron2-Pytorch/tree/main/Apparel_Detection_detectron2) and the colab notebook [here](https://colab.research.google.com/drive/1Wye-IVFSqfBm26TK4d-9hqLl21_P_Zzx?usp=sharing)