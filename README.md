# Automatic Number Plate Recognition (ANPR) System

## Introduction

Number plates are essential for vehicle identification across the nation. Recognizing and detecting number plates is crucial for camera surveillance-based security systems. This method aids in the identification of both authorized and unauthorized vehicles.

## Image Processing & Plate Localization

The image processing and plate localization involve several key stages:

1. **RGB to Gray scale conversion:** Convert the image to grayscale for further processing.

2. **Detection of Plate Size:** Identify and isolate the region containing the number plate.

3. **Dilation of BGM (Binary Gradient Masking):** Enhance the features of the number plate region.

4. **Media Filtering:** Apply filtering techniques to improve image quality.

5. **Eroding of Image:** Remove unnecessary details from the image.

6. **Multiplication of segmented image with gray scale image:** Combine the segmented image with the grayscale image to extract the number plate.

## Character Segmentation

Segmentation is a critical step in number plate recognition:

- **Bounding Box Technique:** Create bounding boxes over each character and number on the plate for individual recognition.

## Character Recognition

Recognize each character on the number plate by comparing it against a complete alphanumeric database using template matching.

## Important MATLAB Functions and Formulas Used

1. `gray=0.114*R+0.587*G+0.299*B`: Convert RGB to grayscale.

2. `I = rgb2gray(RGB)`: Convert a true-color image to grayscale.

3. `BW2 = imfill(BW, 'holes')`: Fill holes in a binary image.

4. `imclearborder(I)`: Suppress structures in the image connected to the border.

## Applications

The ANPR system has various applications, including:

- **Parking:** Allows entry for prepaid members.

- **Tolling:** Calculates travel fees on toll roads and double-checks tickets.

- **Border Security:** Monitors vehicle crossings within and between borders.

- **Traffic Control:** Directs vehicles to different lanes based on their entry permits.

- **Airport Parking:** Reduces ticket fraud and captures vehicle and number plate images.

## Challenges and Considerations

The system may face challenges such as:

1. Broken number plates.

2. Blurry images.

3. Number plates not within legal specifications.

4. Low resolution of characters.

5. Poor maintenance of vehicle plates, leading to similarities between certain characters (e.g., O & D).

_Note: This readme file provides an overview of the ANPR project, its components, and applications. Ensure that the necessary MATLAB functions and formulas are understood and implemented for successful execution._
