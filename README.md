# EXP.3  Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:

## Developed By: Kanishka V S
## Register Number: 212222230061
# Input Grayscale Image and Color Image:
```py
import cv2
import matplotlib.pyplot as plt
Gray_image = cv2.imread('tree.jpg')
Color_image = cv2.imread('york.jpg')
plt.imshow(Gray_image)
plt.show()
plt.imshow(Color_image)
plt.show()
```
# Histogram of Grayscale Image and Green channel of Color Image:
```py
hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
hist1 = cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()
plt.figure()
plt.title("Histogram of Color Image Green Channel")
plt.xlabel('Intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()
```
# Histogram Equalization of Grayscale Image:
```py
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
```
## Output:
### Input Grayscale Image and Color Image:
![image](https://github.com/kanishka2305/Histogram-of-an-images/assets/113497357/7aaaa316-3331-4627-8d8a-0bf5fb78dc95)

### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/kanishka2305/Histogram-of-an-images/assets/113497357/d0715e80-2d38-49c7-9390-87ba9f6e5e2b)

### Histogram Equalization of Grayscale Image.
![image](https://github.com/kanishka2305/Histogram-of-an-images/assets/113497357/dab2a12e-fa77-42fd-824a-f2fa503c5d62)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
