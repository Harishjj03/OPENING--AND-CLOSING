# OPENING--AND-CLOSING
### Name - HARISHBALA J
### Register Number - 212224223002
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

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create a blank image

image = np.zeros((500, 500, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'HASNA', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

# Create the structuring element
kernel = np.ones((3, 3), np.uint8)

# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')


# Opening is erosion followed by dilation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

# Display the result of Opening
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')




# Closing is dilation followed by erosion
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
# Display the result of Opening
plt.imshow(cv2.cvtColor(closed_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Closing Operation")
plt.axis('off')

```
## Output:

### Display the input Image
<img width="532" height="506" alt="Screenshot 2026-03-13 175416" src="https://github.com/user-attachments/assets/58ba042a-6a15-4e5e-8f25-5cd62b251d4a" />




### Display the result of Opening
<img width="496" height="507" alt="Screenshot 2026-03-13 175422" src="https://github.com/user-attachments/assets/b2f9fe91-dfba-48fb-a087-386bc3e66c7c" />


### Display the result of Closing
<img width="517" height="516" alt="Screenshot 2026-03-13 175428" src="https://github.com/user-attachments/assets/ef8da732-f50e-4510-86e6-b561536dd08e" />


<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
