#### Solution for AI4AV assignment 

Detecting Traffic Lights using YOLO algorithm

The YOLO algorithm is a cutting edge technology for object detection and localisation

I trained the YOLO model on Bosch dataset with YOLO's pre-trained weights loaded on it

For this, I first cloned Bosch's bstld repo which has scripts to convert the label into YOLO format

Next was to change classes in the YOLO categorie config config files. The classes were as follows 

RedLeft
Red
RedRight
GreenLeft
Green
GreenRight
Yellow
off

Next, due to computational limitations, I trained the model only on 7000 images during which I achieved an mAP for 0.37

The best result of predictions is shown below 

[! sample prediction][https://github.com/deveshdatwani/ai4av-assignment/blob/master/images.jpeg]
