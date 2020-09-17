# This document contains the details of the dependencies and steps needed to run the project.

## 1. Dependencies required to install to run this project
### a. About LSD-SLAM

(1) Ubuntu 14.04 install of ROS Indigo (Tutorials)
Address:http://wiki.ros.org/indigo/Installation/Ubuntu

(2) Run LSD-SLAM tutorials
Address:https://github.com/tum-vision/lsd_slam

### b. CALC (DeepLCD)

(1) Caffe installation on Ubuntu 14.04 (CPU) 
Tutorial-address:https://topic.alibabacloud.com/a/ubuntu1404-build-caffe-cpu-only-detailed-tutorial-_linux_8_8_20110767.html

(2) Run DeepLCD tutorial
Address:https://github.com/rpng/calc

The steps of running the project have been described in detail in the article. 
It is important to emphasize the issues concerning the download and path configuration of the CALC training model.
This is a very important issue. If an error occurs, our system will not work.

## 2. Download and path configuration of the CALC training model

1. There is a file named "get_model.sh" in our code folder, please run this file in the terminal in order to download the two training model files needed in Caffe.

2. When we finish downloading, please put the folder with these two models into the root directory of Caffe.

3. In this step, please copy the absolute path of Caffe and use it to replace the value of "cafferoot" in the TrackableKeyFrameSearch.h file.

4. After changing the value of the cafferoot parameter, please recompile our project and run it again.
