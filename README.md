# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:

Import the necessary packages.

### Step2:

Create the text image using cv2.putText().

### Step3:

Create the structuring kernel for image dilation and erosion.

### Step4:

Apply erosion and dilation using cv2.erode and cv2.dilate.

### Step5:

Plot the images using plt.imshow().

 
## Program:
```Python
Developed By: Pragatheesvaran AB
Register  No: 212221240039
```

``` Python
# Import the necessary packages

import cv2
import numpy as np
from matplotlib import pyplot as plt

# Create the Text using cv2.putText

# Create the text using cv2.putText
text_image = np.zeros((100,250),dtype = 'uint8')
font = cv2.FONT_HERSHEY_COMPLEX_SMALL
cv2.putText(text_image,"Pranave",(5,70),font,2,(255),2,cv2.LINE_AA) 
plt.title("Original Image")
plt.imshow(text_image,'bone')
plt.axis('off')

# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(4,4))


# Erode the image

image_erode = cv2.erode(text_image,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,'bone')
plt.axis('off')


# Dilate the image

image_dilate = cv2.dilate(text_image,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,'bone')
plt.axis('off')



```
## Output:

### Display the input Image
![praga1](https://github.com/praga-16/Implementation-of-Erosion-and-Dilation/assets/95266924/143d2c7c-c1a5-43ed-9f7f-03b97a651249)



### Display the Eroded Image

![praga2](https://github.com/praga-16/Implementation-of-Erosion-and-Dilation/assets/95266924/c87f358e-4c20-424e-b191-669aea56b484)


### Display the Dilated Image

![praga3](https://github.com/praga-16/Implementation-of-Erosion-and-Dilation/assets/95266924/d87059b2-419a-40b2-bd2e-c41c0ae1d882)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
