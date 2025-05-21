# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm
### Step1:
Translation moves the image along the x or y-axis.

### Step2:
Scaling resizes the image by scaling factors.

### Step3:
Shearing distorts the image along one axis.

### Step4:
Reflection flips the image horizontally or vertically.

### Step5:
Rotation rotates the image by a given angle.


## Program
### Name: Swaminathan.V
### Register Number: 212223110057
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('oph.jpg') 
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  
plt.title("Original Image")
plt.axis('off')
plt.show()

_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)
_, otsu_thresholded = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')
plt.show()

plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')
plt.show()

plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')
plt.show()
```
## Output
### Original Image
![original ](https://github.com/user-attachments/assets/816a06e8-2ce9-43bc-a7a5-7e98a53f6176)

### Global Thresholding
![global](https://github.com/user-attachments/assets/678b5f68-9899-47d1-aaa3-d949e3205d05)


### Adaptive Thresholding
![Adaptive](https://github.com/user-attachments/assets/b3db81ea-b26f-47cc-b688-c4d95d46b4b2)


### Optimum Global Thesholding using Otsu's Method
![otsu](https://github.com/user-attachments/assets/802a1c52-1d37-41b0-87e1-219642dedc1b)


## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
