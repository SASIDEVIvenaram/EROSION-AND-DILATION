# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary libraries (OpenCV and NumPy).

### Step2:
Use cv2.putText to add the text to the img1 image at specific coordinates.

### Step3:
Define two kernels (kernel and kernel1) for morphological operations.

### Step4:
Display the eroded image using cv2.imshow.

### Step5:
Use cv2.waitKey(0) to wait for a key press indefinitely.

 
## Program:

``` Python
# Import the necessary packages

import cv2
import numpy as np

# Create the Text using cv2.putText

img1=np.zeros((100,400),dtype="uint8")
font=cv2.FONT_HERSHEY_PLAIN
cv2.putText(img1,"Sasidevi.V",(5,70),font,2,(255),5,cv2.LINE_AA)
cv2.imshow("image",img1)
cv2.waitKey(0)

# Create the structuring element

kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image

cv2.erode(img1, kernel)
image_erode = cv2.erode(img1,kernel1)
cv2.imshow("Sasidevi.V-212222230136",image_erode)
cv2.waitKey(0)


# Dilate the image
image_dilatel=cv2.dilate(img1,kernel1)
cv2.imshow("Sasidevi.v-212222230136",image_dilatel)
cv2.waitKey(0)

```
## Output:

### Display the input Image
![image](https://github.com/SASIDEVIvenaram/EROSION-AND-DILATION/assets/118707332/4e966111-3605-4284-b72f-fa34d42c8b40)

### Display the Eroded Image
![image](https://github.com/SASIDEVIvenaram/EROSION-AND-DILATION/assets/118707332/66e56017-fbf3-4e6e-a9ca-768496c0fa54)


### Display the Dilated Image
![image](https://github.com/SASIDEVIvenaram/EROSION-AND-DILATION/assets/118707332/4122b66f-8e22-42fb-898d-68a2bbad0222)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
