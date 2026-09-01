# EXPT-8-DIPT
## Image Segmentation Using Thresholding Techniques in OpenCV
## Aim
To segment an image using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques using Python and OpenCV.

The program performs the following operations:

Global Thresholding
Adaptive Thresholding
Otsu's Thresholding
Software Used
Anaconda – Python 3.7
Jupyter Notebook / VS Code
OpenCV (cv2)
NumPy
Matplotlib

## Algorithm
## Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

## Step 2:
Load the input image using OpenCV.

## Step 3:
Convert the input image into grayscale format.

## Step 4: Global Thresholding
Select a fixed threshold value.
Apply thresholding to separate foreground and background pixels.
Display the thresholded image.
## Step 5: Adaptive Thresholding
Compute threshold values for small regions of the image.
Apply Adaptive Mean Thresholding.
Apply Adaptive Gaussian Thresholding.
Display the segmented images.
## Step 6: Otsu's Thresholding
Automatically determine the optimal threshold value.
Apply Otsu's thresholding technique.
Display the segmented image.
## Step 7:
Compare the results obtained from Global, Adaptive, and Otsu's thresholding methods.

## Program
## Developed By
## Name: KAYALVIZHI.V

## Register No:212225040182
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
```
image = cv2.imread('Qn8_thresholding.tif')  # Replace with your image file path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)  # Convert to grayscale
```
```
plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB)) 
plt.title("Original Image")
plt.axis('off')
```
```
_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)
```
```
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)
```
```
_, otsu_thresholded = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
```
```
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')
```
```
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')
```
```
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')
```
```
plt.tight_layout()
plt.show()
```

## Output
<img width="745" height="353" alt="image" src="https://github.com/user-attachments/assets/fbc69156-1b14-4eaa-9497-ff3236dae2a7" />


<img width="675" height="580" alt="image" src="https://github.com/user-attachments/assets/4139f991-626c-480b-a8a5-28a1899d7076" />

## Result

Thus, image segmentation is successfully performed using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques in OpenCV.



