# OPENING AND CLOSING

## AIM:
To implement Opening and Closing using Python and OpenCV.

## SOFTWARE REQUIRED:
1. Anaconda - Python 3.7
2. OpenCV
## ALGORITHM:
### Step 1:
Import the necessary packages.
### Step 2:
Create the Text using cv2.putText
### Step 3:
Create the structuring element.
### Step 4:
Use Opening operation.
### Step 5:
Use Closing Operation.

## PROGRAM:
```
/*
Developed by   : Marella Dharanesh
Register Number: 212222240062
*/
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'DHARANESH',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(img)
plt.show()

# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

# Use Opening operation
image_open=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
plt.axis('off')
plt.imshow(image_open)
plt.show()

# Use Closing Operation
image_close=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
plt.axis('off')
plt.imshow(image_close)
plt.show()

```
## OUTPUT:

### Display the input Image

![download](https://github.com/MarellaDharanesh/Opening-and-Closing/assets/118707669/8dafd4fa-3657-468a-8b65-d7d22d5cf37e)


### Display the result of Opening


![download](https://github.com/MarellaDharanesh/Opening-and-Closing/assets/118707669/cfd844c2-4b0f-47ff-936d-67df549cdb84)


### Display the result of Closing

![download](https://github.com/MarellaDharanesh/Opening-and-Closing/assets/118707669/6f39a181-37a3-4c1c-92cb-3531965848d8)



## RESULT:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
