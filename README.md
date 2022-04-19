### NOTE:

I have ignored the dataset files in gitignore folder as they are too large for a github repo. The data directory also contain some cfg files which are essential to build the solution and train YOLO.

![sample0](https://raw.githubusercontent.com/deveshdatwani/ai4av-assignment/master/yologo_2.png)

## Overview of Solution for AI4AV assignment 
Detecting Traffic Lights using YOLO algorithm

The YOLO algorithm is a cutting edge technology for object detection and localisation

I trained the YOLO model on Bosch dataset with YOLO's pre-trained weights loaded on it

For this, I first cloned Bosch's bstld repo which has scripts to convert the label into YOLO format


### Steps in training YOLO model on Bosch dataset

1. Prepare the dataset by extracting the images in rgb/train files
2. clone bosch's git repo on traffic light detection
3. Create a traffic-lights folder under YOLO's darknet repo and convert VOC labels to YOLO type labels using the voc_label.py script.
4. Change YOLO classes only to traffic lights
5. Split the dataset into train and test split using the train_test_split module written
6. This creates train.txt and test.txt



### Config

classes in the YOLO categorie config config files were altered as following. 

RedLeft
Red
RedRight
GreenLeft
Green
GreenRight
Yellow
off

To load configs from darknet framework

``` 
cp ../cfg/yolov3-tiny.cfg yolov3-tiny-bosch.cfg

```

Due to computational limitations, I trained the model only on 7000 images during which I achieved an mAP for 0.37

### Sample Prediction

![sample](https://raw.githubusercontent.com/deveshdatwani/ai4av-assignment/master/images.jpeg)

### To load weights on YOLO 

```
./darknet detector train traffic-lights/voc-bosch.data traffic-lights/yolov3-tiny-bosch.cfg darknet53.conv.74
```
