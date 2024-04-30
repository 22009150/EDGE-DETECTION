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

## Program:
```
Developed by :ARCHANA K
Register no:212222240011
```
### Convert image to grayscale and remove noise
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("dip6.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
### SOBEL EDGE DETECTOR
SOBEL X AXIS:
```
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
SOBEL Y AXIS:
```
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()

```
SOBEL XY AXIS:
```
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
### LAPLACIAN EDGE DETECTOR:
```
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
### CANNY EDGE DETECTOR:
```
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:

![Screenshot (133)](https://github.com/22009150/EDGE-DETECTION/assets/118708624/39889770-1e7d-4217-8daa-c018883200bd)

### SOBEL EDGE DETECTOR
### SOBEL X AXIS:

![Screenshot (134)](https://github.com/22009150/EDGE-DETECTION/assets/118708624/f952324e-69fd-44c8-a073-67b38024bf22)

### SOBEL Y AXIS:
![Screenshot (135)](https://github.com/22009150/EDGE-DETECTION/assets/118708624/1b89a0f6-4926-4e03-a0fe-21e377dcdcb0)



### SOBEL XY AXIS:

![Screenshot (136)](https://github.com/22009150/EDGE-DETECTION/assets/118708624/38ba9019-f695-4f17-b9fa-63fd5383992d)


### LAPLACIAN EDGE DETECTOR:

![Screenshot (137)](https://github.com/22009150/EDGE-DETECTION/assets/118708624/2d03488c-5053-4871-92de-f2c14c9a7799)


### CANNY EDGE DETECTOR
![Screenshot (138)](https://github.com/22009150/EDGE-DETECTION/assets/118708624/8931c6ad-78d1-443d-bbc7-78e5d005a18a)



## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
