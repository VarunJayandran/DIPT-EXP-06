# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:
Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## PROGRAM:

Developed by : VARUN JC


Reg no : 212224240179

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('my image.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
### Output:

<img width="372" height="511" alt="image" src="https://github.com/user-attachments/assets/cc991fb4-01cc-4f85-8766-0b49ad297911" />


## SOBEL EDGE DETECTOR

### Program:
```python
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
### Output:
<img width="357" height="521" alt="image" src="https://github.com/user-attachments/assets/af9a9fdb-f0cb-46ee-98a1-16013e3da952" />


## LAPLACIAN EDGE DETECTOR
### Program:
```python
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
### Output:
<img width="365" height="517" alt="image" src="https://github.com/user-attachments/assets/b4811c4f-ca61-46c2-942a-769ddc06cbca" />


## CANNY EDGE DETECTOR
### Program:
```python
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
### Output:
<img width="363" height="507" alt="image" src="https://github.com/user-attachments/assets/1c36ace1-4ba7-4492-9f01-a77eba127161" />


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
