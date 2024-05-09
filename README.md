# EX03 Histogram-of-an-images
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
# Developed By: JANARTHANAN V K
# Register Number: 212222230051
### Input Grayscale Image and Color Image
```
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("gray.jpg")
color_image = cv2.imread("color.jpg")
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Color Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


### Histogram of Grayscale Image and any channel of Color Image
```
import numpy as np
import cv2
Gray_image = cv2.imread("gray.jpg")
Color_image = cv2.imread("color.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```

## Histogram Equalization of Grayscale Image.
```python
import cv2
gray_image = cv2.imread("gray.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image:

<img src="https://github.com/Janarthanan2/DIP_EX03_Histogram-of-an-images/assets/119393515/8a938518-0869-46df-bcb9-9aa9d2a2e98a" width = 150 height =250>
<img src="https://github.com/Janarthanan2/DIP_EX03_Histogram-of-an-images/assets/119393515/7b2db2a7-0c3c-43fd-bed3-37c9cdab2395" width = 35%>




### Histogram of Grayscale Image and any channel of Color Image


![Screenshot 2024-03-19 111104](https://github.com/Aravindsamy04/Histogram-of-an-images/assets/113497037/496e3f97-2b4c-44c3-8fbd-1445e7b46578)






## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
