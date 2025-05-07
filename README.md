# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm :
### Step 1 :

Import the necessary pacakages

### Step 2 :

Create the text using cv2.putText

### Step 3 :

Create the structuring element


### Step 4 :

Erode the image

### Step 5 :

Dilate the image

## Program :

```
# Import the necessary packages
import cv2
import numpy as np
from matplotlib import pyplot as plt
# Load the image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL


# Create the Text using cv2.putText
cv2.putText(img1,'Priya' ,(5,70),font,4,(255),2,cv2.LINE_AA)

# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)

# Erode the image
img_erode=cv2.erode(img1,kernel1)

# Display the results
plt.figure(figsize=(10, 9))
plt.subplot(1,3,1)
plt.imshow(img1,cmap='gray')
plt.subplot(1,3,2)
plt.imshow(img_dilate,cmap='gray')
plt.subplot(1,3,3)
plt.imshow(img_erode,cmap='gray')

```
## Output :

### Display the input Image

![image](https://github.com/user-attachments/assets/ae2e9b3a-f6fb-4380-9e15-af82840f8bdc)

<br>

### Display the Dilated Image

![image](https://github.com/user-attachments/assets/8ba56666-3986-46ce-83b5-24baee5e3861)

<br>

### Display the Eroded Image

![image](https://github.com/user-attachments/assets/42ffa216-4f24-47fd-8c5d-a1e466096ecd)

<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
