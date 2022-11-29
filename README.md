# Crowd Counting using Image Processing Techniques
This repository contains code for my image processing course project. The objective is to count the number of people in the given images by using classical image processing techniques. The idea is to develop an algorithm from the basics without using neural networks.

## Repository Structure
This repository contains the following folders and files:
* images: this directory contains 10 images provided for the problem
* labels.csv: This csv file contains the ground truth annotations created using Makesense.ai
* annotations.csv: This csv file contains some patches from the image background which are used to train the HOG classifier.
* CrowdCounting.ipynb: This is the main notebook which contains the entire solution pipeline
* Feature_Matching.ipynb: This notebook contains detailed experiments with HOG classifier

## How to Run
I mostly worked on colab for this project. In order to run these notebooks, the easier way is to use colab and upload the images folder along with the annotations files there.

##Algorithm
The main pipeline of the algorithm is shown in the figure below
![image](https://user-images.githubusercontent.com/30044227/204503797-21abf011-e036-4072-8de8-821bcadf88be.png)

The central idea is to estimate the background, subtract it from the image and threshold the resultant to create a binarized image. This binarized image is processed to find contours and ultimately the bounding boxes.

## Results
Different techniques have been tried which can be explored in the Colab notebook. The results across different techniques have been compared namely: OpenCV KNN background subtraction (with and without CLAHE), represented in the graphs as KNN BG and KNN BG+CLAHE, Median and mean background estimation (with and without CLAHE), represented by the name Median BG, Mean BG, Median BG+CLAHE and Mean BG+CLAHE, results after post-processing techniques, HOG classification and K means clustering, which are represented as HOG and KMeans 1. The quantitative results of the image have been calculated on two levels: Image level and Person level. 

### Image Level Results
![image](https://user-images.githubusercontent.com/30044227/204503968-9b27d44e-7869-4f6f-bb09-ed1354717a08.png)


### Person Level Results
<img width="541" alt="image" src="https://user-images.githubusercontent.com/30044227/204504573-cf694c7b-6577-4e16-9bf2-f83c304baebe.png">


