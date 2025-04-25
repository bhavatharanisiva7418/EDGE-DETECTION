# EDGE-DETECTION
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

## PROGRAM:
## Devloped By:BHAVATHARANI S
## Register NO:212223230032

## Original
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread("bird.jpg")
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

### ORIGINAl

![image](https://github.com/user-attachments/assets/6540cc4b-6b29-480b-b926-20c7884f7ff1)


### SOBEL EDGE DETECTOR

![image](https://github.com/user-attachments/assets/a475f349-4191-4175-aaaa-a6e49b2c63c2)


### LAPLACIAN EDGE DETECTOR

![image](https://github.com/user-attachments/assets/7ce7614e-4cbd-443d-9e78-3fcb4247e560)


### CANNY EDGE DETECTOR

![image](https://github.com/user-attachments/assets/ea6b2fb8-faec-4e0e-88dc-f43031394aca)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
