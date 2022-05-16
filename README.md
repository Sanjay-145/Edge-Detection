# Edge-Detection
## Aim:

To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary modules.
<br>


### Step2:
For performing edge detection on a image.

* Sobel
```
sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,5)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,5)
sobelxy=cv2.Sobel(img,cv2.CV_64F,1,1,5)
```

* Laplacian
```
Laplacian=cv2.Laplacian(img,cv2.CV_64F)
```

* Canny
```
canny=cv2.Canny(img,120,150)
```
<br>

### Step3:
Display all the images with their respective edge detected images.
<br>
 
# Program:
## Developed By : P.Sanjay
## Register Number: 212220230042

# Import the packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
# Load the image, Convert to grayscale and remove noise
```
image1=cv2.imread ('coco.jpg') 
gray_image = cv2.cvtColor(image1,cv2.COLOR_BGR2GRAY)

plt.title('GRAY IMAGE')
plt.imshow(gray_image,cmap = 'gray')
```
# SOBEL EDGE DETECTOR
```
img = cv2.GaussianBlur(gray,(3,3),0)
sobelx = cv2.Sobel(gray_image,cv2.CV_64F,1,0,ksize=5)
sobely = cv2.Sobel(gray_image,cv2.CV_64F,0,1,ksize=5)
sobelxy =cv2.Sobel(gray_image,cv2.CV_64F,1,1,ksize=5)
plt.figure(1)
plt.subplot(2,2,1)
plt.imshow(gray_image,cmap = 'gray')
plt.title('Original'), plt.xticks([]), plt.yticks([])

plt.subplot(2,2,2)
plt.imshow(sobelx,cmap='gray')
plt.title('sobelx')
plt.xticks([]), plt.yticks([])

plt.subplot(2,2,3)
plt.imshow(sobely,cmap='gray')
plt.title('sobely')
plt.xticks([]), plt.yticks([])

plt.subplot(2,2,4)
plt.imshow(sobelxy,cmap='gray')
plt.title('sobelxy')
plt.xticks([]), plt.yticks([])
plt.show()
```
# LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image,cv2.CV_64F)
plt.imshow(laplacian,cmap='gray')
plt.title('laplacian')
plt.show()
```
# CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 120, 150)
plt.imshow(canny_edges,cmap='gray')
plt.title('canny_edges')
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR

![s2](https://user-images.githubusercontent.com/75235426/168647242-075a521b-381c-4f16-b1d1-906ce85b2f73.jpg)

### LAPLACIAN EDGE DETECTOR

![s3](https://user-images.githubusercontent.com/75235426/168647258-b8c4665c-2a7d-4163-b1fb-16095d6ef843.jpg)

### CANNY EDGE DETECTOR

![s4](https://user-images.githubusercontent.com/75235426/168647277-579c1bfb-3a5f-4bcc-a076-a549b3092041.jpg)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
