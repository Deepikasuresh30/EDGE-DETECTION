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

# Program 
## Developed By: Deepika S
## Reg NO: 212223230039

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread("C:/Users/admin/Downloads/Bird.jpg")  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```
# Output

![image](https://github.com/user-attachments/assets/7bd520c3-2154-4f9d-a76c-38d25c2f2e78)

![image](https://github.com/user-attachments/assets/f0b38419-8744-432b-95a1-99be2663a136)

![image](https://github.com/user-attachments/assets/08a560cb-20a9-4ac6-b8bc-8c18a78f16dd)

![image](https://github.com/user-attachments/assets/03ab6ad9-ef73-454d-afc5-52f4660f57ed)


# Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
