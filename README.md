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
# Developed By: BALA MURUGANS S
# Register Number: 212223230027
```
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
```
image = cv2.imread('a.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
```
```
equalized_image = cv2.equalizeHist(gray_image)
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.figure(figsize=(10, 7))
```
```
plt.subplot(2, 2, 1)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
```
plt.subplot(2, 2, 2)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')
```
```
plt.subplot(2, 2, 3)
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
```
plt.subplot(2, 2, 4)
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```
```
plt.tight_layout()
plt.show()
```
  
## Output:
### Input Grayscale Image and Color Image

<img width="229" height="191" alt="image" src="https://github.com/user-attachments/assets/f04a499f-2cc4-4d17-b8ec-16e0e8db208b" />


<img width="168" height="198" alt="image" src="https://github.com/user-attachments/assets/617a22dc-8eeb-4470-acac-73a76bd7b0e9" />





### Histogram of Grayscale Image and any channel of Color Image


<img width="319" height="230" alt="image" src="https://github.com/user-attachments/assets/e62f1342-8d1f-4c68-af3d-4333f2e461db" />





### Histogram Equalization of Grayscale Image.

<img width="302" height="225" alt="image" src="https://github.com/user-attachments/assets/d76ea410-42b0-4f5d-bea3-e775daf82a0f" />






## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
