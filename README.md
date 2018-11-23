# IET-video-autosegmentation
Automatic object segmentation and blurring program for videos. 

By running the code, you will be able to select a target character in a video clip and use Gaussian blur to mask out the face and body of the target character, or mask out surrounding regions except the character.

Image 1: Original frame

<img src="https://i.imgur.com/FC58E4t.jpg" width="300"/>

Image 2: Target character masked out

<img src="https://i.imgur.com/zs8gsLB.jpg" width="300"/> 
 
Image 3: Surrounding region (context) masked out:

<img src="https://i.imgur.com/gMxibiM.jpg" width="300"/>

## Requirements
This project is based on the state-of-the-art object detection and segmentation models made available by ['Google Object Dection API'](https://github.com/tensorflow/models/tree/master/research/object_detection). To run the model, you will need to follow [the installation guide](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/installation.md) here to make sure everything is properly installed. You will also need additional packages like [scikit-image](http://scikit-image.org/docs/dev/install.html), glob, etc.. It is recommended that you run STEP 2 on a PC (or a cloud machine) with a good GPU.

## How it works
The code has four parts, written in seperate jupyter notebooks

STEP 1. Generate frames from video file.

STEP 2, Run the object detection and segmentation model on the frames and save the results.

STEP 3, Select the target character to mask on key frames.

STEP 4, Apply temporal smoothing to the masks and regenerate the blurred video.


## About the author
The current repo is maintained by:
Zhimin Chen (https://mandyzchen.github.io/)
