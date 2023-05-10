# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step1:
Import the necessary packages.<br>
### Step2:
Create the Text using cv2.putText.
### Step3:
Create the structuring element.
### Step4:
Use Opening operation.
### Step5:
Use Closing Operation.
Print the output and end the program.
 
## Program:

``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
name = np.zeros((100,440),dtype='uint8')
font = cv2.FONT_HERSHEY_COMPLEX
image = cv2.putText(name,'Y SHAVEDHA',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(image)

# Create the structuring element
Kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation
image1=cv2.morphologyEx(image,cv2.MORPH_OPEN,Kernel)
plt.imshow(image1)

# Use Closing Operation
image1 = cv2.morphologyEx(image,cv2.MORPH_CLOSE,Kernel)
plt.imshow(image1)

```
## Output:

### Display the input Image
<img width="521" alt="image" src="https://github.com/Shavedha/Opening-and-Closing/assets/93427376/904c1746-6c7e-4ffc-afde-3d68ecbc8859">


### Display the result of Opening
<img width="534" alt="image" src="https://github.com/Shavedha/Opening-and-Closing/assets/93427376/933e164c-d84b-4fd9-b913-5cd68c935328">


### Display the result of Closing
<img width="520" alt="image" src="https://github.com/Shavedha/Opening-and-Closing/assets/93427376/bd355364-914f-42d2-8120-819b5a8ded3b">


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
