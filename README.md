# EXP-6 EDGE-DETECTION
# NAME: MANIKUMAR D.K
# REG NO: 212223230121
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:
### ORIGINAL IMAGE
```
NAME : PAVITHRAN MJ
REG NO : 212223240112



import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('111.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
## Output:
### SOBEL EDGE DETECTOR
<img width="297" height="411" alt="download" src="https://github.com/user-attachments/assets/46ab3f73-4213-44b5-844e-16453a97068d" />



### LAPLACIAN EDGE DETECTOR
<img width="297" height="411" alt="download" src="https://github.com/user-attachments/assets/90d0f9a1-d293-4907-88e9-14bb735c8a0f" />



### CANNY EDGE DETECTOR
<img width="297" height="411" alt="download" src="https://github.com/user-attachments/assets/bddd614a-ac09-4f6d-b895-430b378c53f6" />



## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
