# EX 10 OPENING AND CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
- Step1: Import the necessary packages
- Step2: Give the input text using cv2.putText()
- Step3: Perform opening operation and display the result
- Step4: Similarly, perform closing operation and display the result
## Program:
```
NAME: Santhosh U
REG.No:212222240092
``` 
# Import the necessary packages
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```python
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'Greedy',(5,70), font,2,(255),5,cv2.LINE_AA)
```
# Create the structuring element
```python
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
# Use Opening operation
```python
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")
```
# Use Closing Operation
```python
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
```
## Output:
### Display the input Image
![Output1](https://github.com/SanthoshUthiraKumar/OPENING--AND-CLOSING/assets/119477975/bb76105b-2010-4314-b6fa-fd2833b4f148)

### Display the result of Opening
![Output2](https://github.com/SanthoshUthiraKumar/OPENING--AND-CLOSING/assets/119477975/61613e9a-670b-45a1-bbc2-961e6c9fe115)

### Display the result of Closing
![Output3](https://github.com/SanthoshUthiraKumar/OPENING--AND-CLOSING/assets/119477975/2a74a628-6565-4598-b2c0-4f4f96499553)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
