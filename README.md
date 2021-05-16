# ANPR-System

Automatic number-plate recognition (ANPR) is a technology that uses optical character recognition on images to read vehicle registration plates and store vehicle information. 

# Steps Involved

## License Plate Detection

## Image Pre-processing

## Character Segmentation

## Character Recognition

# File Structure

data.ipynb : to read and convert training data from csv to yolo readable format

data_test.ipynb : to read xml image files and convert them to yolo format , also created labels used for testing of each image

label_img : to label each vehicle's license manually

yolov5.ipynb : to train the model on yolov5 and detect the license plate of vehicle in each image

char_recog.ipynb  : to train the lenet model for character recognition

run.ipynb : to run all individual steps like detection, image processing, segmentation and recognition on a sample test

run_all.ipynb : to run the complete model and return the summary of it's execution



