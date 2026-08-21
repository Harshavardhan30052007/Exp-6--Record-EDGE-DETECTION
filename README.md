# Exp-6--Record-EDGE-DETECTION
# Edge-detection-opencv
## Aim
To perform edge detection using Sobel, Roberts, Prewitt, Laplacian, and Canny edge detectors.

## Software Required
Anaconda – Python 3.7
Jupyter Notebook / VS Code
OpenCV (cv2)
NumPy
Matplotlib
##  Algorithm
Step 1:
Import all the necessary modules for the program.

Step 2:
Load an image using cv2.imread().

Step 3:
Convert the image to grayscale.

Step 4:
Apply Sobel operator using OpenCV to detect edges.

Step 5:
Apply Prewitt operator using custom kernels.

Step 6:
Apply Roberts operator using custom kernels.

Step 7:
Apply Laplacian operator using OpenCV.

Step 8:
Apply Canny edge detector using OpenCV.

Step 9:
Display all edge-detected images for comparison.

# PROGRAM :
```
1.
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread(r"C:\Users\admin\Music\eleharsha6.webp")  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
```
2.
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
```
3.
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
```
4.
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```

# Name: HARSHAVARDHAN K B
# Register No: 212224240054


## Output

<img width="641" height="461" alt="image" src="https://github.com/user-attachments/assets/2222129c-28ed-45d9-944d-64cce2353ca8" />

<img width="642" height="458" alt="image" src="https://github.com/user-attachments/assets/bbb3e983-1403-4c84-899c-4687e8177c52" />

<img width="640" height="456" alt="image" src="https://github.com/user-attachments/assets/f2cacd3f-8cfc-4f78-8b5f-5117cc2b415f" />

<img width="642" height="461" alt="image" src="https://github.com/user-attachments/assets/6cd54d2f-ea96-446c-8249-9064ca4b0ec9" />


## Result
Thus, edges are successfully detected using Sobel, Prewitt, Roberts, Laplacian, and Canny edge detection techniques. Each method highlights edges differently based on gradient and intensity variations, improving feature extraction and analysis.
