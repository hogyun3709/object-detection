# Object-Detection-fashion

This repository contains sources that helps to build your own object-detection model by using tensorflow. Following two posts help you to understand.

* Conceptual post: <br>
[How to train your own Object Detector with TensorFlow’s Object Detector API](https://towardsdatascience.com/how-to-train-your-own-object-detector-with-tensorflows-object-detector-api-bec72ecfe1d9?fbclid=IwAR28ciB3yWmcRM14p_qGr655YEQVQeF-CAmRxHut2vOnPjQbfbd5JK-anwc)
* Tutorial post: <br>
[TensorFlow Object Detection API Tutorial](https://pythonprogramming.net/video-tensorflow-object-detection-api-tutorial/)

## Understanding object-detection work flow

1. Creating Dataset <br>
  A. Prepare image datasets - Using crawler - [AutoCrawler](https://github.com/YoongiKim/AutoCrawler)<br>
  B. Label the images - Choose image annotation program which helps label the image manually - [LabelImg](https://github.com/tzutalin/labelImg), [RectLabel](https://rectlabel.com/) <br>
  C. Convert xml to csv - xml_to_csv.py
  D. Create TFRecord file - generate_tfrecord.py
  
2. Training the model
  A. Select pretrained model <br>
  B. Create label-map .pbtxt file <br>
  C. Modify coresponding config file of pretrained model <br>
  D. Excute train
  

## Step by Step instruction
 - Clone tensorflow/model directroy from github

1. Installation and compilation <br>
 [Click here to see instructions](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/installation.md) <br>
 
  A. Install dependencies - (tensorflow may not support cuda 10)<br>
  B. Configure protobuf compilation <br>
  C. Add Libraries to PYTHONPATH <br>
  
2. Create your own dataset <br>

  A. Get ready for dataset <br>
    - There are several methods to prepare your own dataset: download images manually, from others researched data or etc. <br>
    - Recommended: Use relevant web crawler: [AutoCrawler](https://github.com/YoongiKim/AutoCrawler)<br>
    1. Download at least 200 images for each label. <br>
    2. Split into train/test folders portion of 150 / 50 images. <br>
    3. Use image annotation tool to create bounding boxes on downloaded images manually. <br>
    4. For each saved image, check out a pair of .xml file and your image file. <br>
    
### To be continue...
    
    
    

  
# Currently solving cuda 10 install issue due to tensorflow 1.13 dependency issue

