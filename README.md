# ANPR-System

Automatic number-plate recognition (ANPR) is a technology that uses optical character recognition on images to read vehicle registration plates and store vehicle information. 

# Steps Involved

 ## 1. License Plate Detection
 Here, we have taken an image as input, and  our task aims to localize the license plate of the vehicle in the image.We will do this using state of the art YOLO deep learning object detection architecture based on Convolutional Neural Networks which will return the bounding box of the plate. 


## 2. Image Pre-processing
The main objective of the preprocessing phase is to make it as easy as possible for the OCR system to distinguish a character/word from the background. 
We will take an image of the license plate as an input, first we will convert the RGB image into GRAY scale and then we will binarize it.


## 3. Character Segmentation
Our next task is to extract the individual characters from the license plate.
For this we searched for contours in the image. Each contour is taken as a single character.

To eliminate noise contours we added various filters based on orientation of the contour. 


 ## 4. Character Recognition
For this  step, we trained a CNN based recognition model on the character dataset, following the lenet architecture. 

Characters generated from the previous step are then fed to this model which return the corresponding labels, which are then combined to give the final output. 

# File Structure

## data.ipynb : 
 to read and convert training data from csv to yolo readable format

## data_test.ipynb : 
to read xml image files and convert them to yolo format , also created labels used for testing of each image

## label_img : 
to label each vehicle's license manually

## yolov5.ipynb : 
to train the model on yolov5 and detect the license plate of vehicle in each image

## char_recog.ipynb  :
to train the lenet model for character recognition

## run.ipynb :
to run all individual steps like detection, image processing, segmentation and recognition on a sample test

## run_all.ipynb :
to run the complete model and return the summary of it's execution



