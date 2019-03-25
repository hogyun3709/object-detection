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
  A. Select pretrained model
  B. Create label-map .pbtxt file
  C. Modify coresponding config file of pretrained model
  D. Excute train
  
