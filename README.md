# Hand-Gesture-Recognition
## Problem Statement & Background
To recognize hand gestures from a real time video sequence following ASL (American Sign Language). <br>
<br>
According to the NAD, 18 million people are estimated to be deaf. They can communicate among themselves using sign language but having a conversation with others is a difficult task. Extensive work has been done on the American Sign Language(ASL) and by working on this project we want to translate the
sign language into text and sound and enable deaf people to have an improved conversational experience.

## Demo

Here is the demo of Hand Gesture Recognition - <br>
<br>
<br>
<p align="center">
  <img src="https://github.com/thota-sasanth/Hand-Gesture-Recognition/blob/master/hand-ges.gif">
</p>
<br>

## Data Preparation / Processing
Created own dataset by following the American Sign Language for alphabets, special characters and also added few custom gestures like YOLO , All the best, etc.. which can be further extended to add more Sign Language Vocabulary. First, we extract the images of hand in grayscale using absolute Background Subtraction Technique (using OpenCV, Tensorflow) which uses the concept of running averages from a sequence of video frames. Then we do thresholding for this image. By this we can get the contour of the hand region. For each gesture we get a threshold image and all these images are pre-processed using Keras preprocessing & image augmentations model which does the necessary resizing, shifts, flips, orientations to certain degree, etc.. which concludes our Final Dataset.
<br>
<br>
<p align="center">
  <img src="https://github.com/thota-sasanth/Hand-Gesture-Recognition/blob/master/hand-data.png" width="700" height="500">
</p>
<br>

## Modeling and Architecture
The model architecture includes the Deep Convolution Neural Network. The network contains 7 hidden convolution layers with Relu as the activation function and 1 Fully connected layer. The network is trained across 50 iterations with a batch size of 64. Since 50 iterations kind of trains the model well and there is no increase in validation accuracy along the lines so those iterations should be enough.
<br>

## Results
This model recognizes hand gestures from a live video sequence. It can predict various signs and gestures with overall accuracy of 92%. It also translates  hand gestures into both text and speech using Python gTTS. It is dynamic as users can create their own custom gestures and then train the model before using those custom gestures.

