# Histogram-of-an-images
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
```python
# Developed By: 
# Register Number: 
```
### Read image

```
import cv2
import matplotlib.pyplot as plt
Gray_image = cv2.imread('i11.jpg')
Color_image = cv2.imread('i22.jpg')
plt.imshow(Gray_image)
plt.show()
plt.imshow(Color_image)
plt.show()
```
### Calculate Hist
```
hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
hist1 = cv2.calcHist([Color_image],[1],None,[256],[0,256])
```
### Histogram for Gray image
```
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()
```
### Histogram for Color image
```
plt.figure()
plt.title("Histogram of Color Image Green Channel")
plt.xlabel('Intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()
```
### Histogram Equalization
```

import cv2
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)

```
## Output
### Input Grayscale Image and Color Image
![image](https://github.com/swedha333/Histogram-of-an-images/assets/118720291/585450ba-ab2b-4b9f-aff8-06591eca0884)


### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/swedha333/Histogram-of-an-images/assets/118720291/34810f2b-5b70-4ade-85d4-9d569f44c0d6)



### Histogram Equalization of Grayscale Image.


![image](https://github.com/swedha333/Histogram-of-an-images/assets/118720291/578fbff7-c425-45bc-a042-5514472daa53)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
