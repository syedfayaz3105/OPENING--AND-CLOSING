
# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:

Create the structuring element.
### Step4:
Use Opening operation.

### Step5:
Use Closing Operation.

 
## Program:
### DEVELOPED BY: Farhana H
### REGISTER NO: 212223230057

# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```


# Create the Text using cv2.putText
```
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'Farhana', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```


# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
```
# Use Opening operation
```
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")

```
# Use Closing Operation
```
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")



```
## Output:

### Display the input Image
<img width="761" height="196" alt="Screenshot 2025-10-18 110835" src="https://github.com/user-attachments/assets/b836fcdb-7439-4fde-95b4-adef4718bc9f" />


### Display the result of Opening
<img width="658" height="180" alt="image" src="https://github.com/user-attachments/assets/6374a9e8-2809-4b4c-99e7-d53eb645bbcd" />



### Display the result of Closing
<img width="761" height="213" alt="Screenshot 2025-10-18 110844" src="https://github.com/user-attachments/assets/c5c56f58-b25c-4813-bca3-dcb36c9c6a7d" />

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
