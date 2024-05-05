# EX 10 OPENING AND CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages
### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation
## Program:
```
Developed by: SANDHIYA R
Register number: 212222230129
```
``` Python
# Import the necessary packages

import cv2
import numpy as np

# Create the Text using cv2.putText

img = np.zeros((350, 1400), dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img, 'ICE AGE', (15, 200), font, 5, (255), 10, cv2.LINE_AA)
cv2.imshow('created_text', img)
cv2.waitKey(0)

# Create the structuring element

struct_ele = np.ones((9, 9), np.uint8)

# Use Opening operation

opening = cv2.morphologyEx(img, cv2.MORPH_OPEN, struct_ele)
cv2.imshow('Opening', opening)
cv2.waitKey(0)


# Use Closing Operation


closing = cv2.morphologyEx(img, cv2.MORPH_CLOSE, struct_ele)
cv2.imshow('Closing', closing)
cv2.waitKey(0)


```
## Output:

### Display the input Image
![326161580-9b01c0f4-42e7-4327-bd9c-fa41e6fbb19f](https://github.com/SandhiyaR1/OPENING--AND-CLOSING/assets/113497571/d0ac4ccc-3137-4914-83d2-84454739fb97)

### Display the result of Opening
![326161438-5f208fb7-7cd7-40d0-8999-13b13ab99f97](https://github.com/SandhiyaR1/OPENING--AND-CLOSING/assets/113497571/e4fe9c99-7786-45f1-b761-c7d27dcc35bc)


### Display the result of Closing
![326161480-5dce3dd4-774f-4ef1-9089-547aa1c2b4f8](https://github.com/SandhiyaR1/OPENING--AND-CLOSING/assets/113497571/9ab59e34-4bb1-44bf-9fa9-2ae11e7bc903)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
