# ANPR-using-ANN-and-SVM

## Overview
This notebook provides an implementation of Automatic Number Plate Recognition (ANPR) to detect automobile license plates in photographs taken within a range of 1-2 meters from a car. The process involves techniques such as image segmentation, feature extraction, pattern recognition, and the use of Support Vector Machines (SVM) and Artificial Neural Networks (ANN).

## Background
Automatic Number Plate Recognition (ANPR) is a surveillance method that utilizes Optical Character Recognition (OCR) and various techniques like segmentation and detection to read vehicle registration plates.

## Dataset
The dataset used here includes license plates from Croatia. While the algorithms are tailored to Croatian license plates, they can be adapted for other countries' specifications.

## Plate Detection
The plate detection process involves several steps:
1. Load Car Image: Visualize the image containing the car.
2. Segmentation: Segment the image to identify possible regions containing license plates.
3. Classification: Classify the segmented regions to identify license plates.

## Segmentation
Segmentation involves identifying potential license plate regions by:
- Converting the image to grayscale.
- Applying Gaussian blur to remove noise.
- Using Sobel filter for edge detection.
- Thresholding to obtain a binary image.
- Performing morphological closing to connect edges.
- Identifying contours to locate possible plate regions.
- Validating contours based on area and aspect ratio.

## Classification
Classification employs SVM to distinguish between positive (license plate) and negative (non-plate) samples.

## Plate Recognition
The plate recognition stage focuses on retrieving characters from the license plate using OCR. It involves:

Segmenting the plate for each character.
Using an ANN for character recognition.

## OCR Segmentation
OCR segmentation involves:
- Validating bounding boxes for characters.
- Training an ANN with a hidden layer for character recognition.

## Conclusion
This notebook demonstrates a comprehensive approach to ANPR, covering plate detection, segmentation, classification, and recognition stages. The techniques showcased here can be extended and adapted for various license plate specifications and countries.
