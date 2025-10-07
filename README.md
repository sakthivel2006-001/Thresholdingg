# NAME: SAKTHIVEL S
# REG NO: 212223220090
# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Load the necessary packages.

### Step2:
Read the Image and convert to grayscale.

### Step3:
Use Global thresholding to segment the image.

### Step4:
Use Adaptive thresholding to segment the image.

### Step5:
Use Otsu's method to segment the image and display the results.
am

# Program:
```
NAME: ASWIN.L
REG NO: 212224230028
# Load the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt



# Read the Image and convert to grayscale
image = cv2.imread('me.jpg')  # Replace with your image file path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)  # Convert to grayscale
plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert from BGR to RGB for display
plt.title("Original Image")
plt.axis('off')


# Use Global thresholding to segment the image
_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)



# Use Adaptive thresholding to segment the image
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)



# Use Otsu's method to segment the image 
_, otsu_thresholded = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)



# Display the results
# Global Thresholding
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')

# Adaptive Thresholding
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')

# Otsu's Method
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')

# Show the plot
plt.tight_layout()
plt.show()

```
## Output

### Original Image
<img width="142" height="210" alt="download" src="https://github.com/user-attachments/assets/dac559d8-03c7-4cb4-b7b8-35182498c479" />


### Global Thresholding
<img width="185" height="210" alt="download" src="https://github.com/user-attachments/assets/5304692b-2810-401a-9b8c-f2e2bf7124fd" />



### Ada<img width="206" height="210" alt="download" src="https://github.com/user-attachments/assets/f2cbd279-39e7-4edd-a1e3-fdf7850e8b45" />
ptive Thresholding

### Optimum Global Thesholding using Otsu's Method
<img width="139" height="210" alt="download" src="https://github.com/user-attachments/assets/2c02ff37-af93-4754-955b-67202e06a92f" />



## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
