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
Gray_image = cv2.imread('tree.jpg')
Color_image = cv2.imread('york.jpg')
plt.imshow(Gray_image)
plt.show()
plt.imshow(Color_image)
plt.show()

```


### Histogram of Grayscale Image and any channel of Color Image
```
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


## Output:
### Input Grayscale Image and Color Image:

<img src="https://github.com/Janarthanan2/DIP_EX03_Histogram-of-an-images/assets/119393515/8a938518-0869-46df-bcb9-9aa9d2a2e98a" width = 150 height =250>
<img src="https://github.com/Janarthanan2/DIP_EX03_Histogram-of-an-images/assets/119393515/7b2db2a7-0c3c-43fd-bed3-37c9cdab2395" width = 35%>




### Histogram of Grayscale Image and any channel of Color Image


![Screenshot 2024-03-19 111104](https://github.com/Aravindsamy04/Histogram-of-an-images/assets/113497037/496e3f97-2b4c-44c3-8fbd-1445e7b46578)






## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
