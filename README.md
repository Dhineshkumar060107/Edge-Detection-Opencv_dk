# Edge-Detection-Opencv


## Aim

To perform edge detection using Sobel, Roberts, Prewitt, Laplacian, and Canny edge detectors.

---

## Software Required

- Anaconda – Python 3.7  
- Jupyter Notebook / VS Code  
- OpenCV (cv2)  
- NumPy  
- Matplotlib  

---

## ⚙️ Algorithm

### Step 1:
Import all the necessary modules for the program.

### Step 2:
Load an image using `cv2.imread()`.

### Step 3:
Convert the image to grayscale.

### Step 4:
Apply **Original Image** using OpenCV to detect edges.

### Step 5:
Apply **Sobel Edge Detector** using custom kernels.

### Step 6:
Apply **Laplacian operator** using OpenCV.

### Step 7:
Apply **Canny edge detector** using OpenCV.

### Step 8:
Display all edge-detected images for comparison.

---

## Developed By

- **Name:** DHINESHKUMAR L
- **Register No:** 212224230066

---

## Output

###  Original Image
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('dk_image.jpeg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
<img width="397" height="517" alt="image" src="https://github.com/user-attachments/assets/9d2feadf-62f3-41d6-9c04-45fd71679336" />


###  Sobel Edge Detector
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
<img width="385" height="511" alt="image" src="https://github.com/user-attachments/assets/2c67804a-e747-42e2-bd3b-6d5da58e6a91" />




###  Laplacian Edge Detector
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
<img width="397" height="516" alt="image" src="https://github.com/user-attachments/assets/cbda4e2d-97fe-4a62-8320-96d3b43f657b" />


###  Canny Edge Detector
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```
<img width="416" height="517" alt="image" src="https://github.com/user-attachments/assets/d52905ae-908c-41f8-93a4-73f3a91d825c" />


## Result

Thus, edges are successfully detected using Sobel, Prewitt, Roberts, Laplacian, and Canny edge detection techniques. Each method highlights edges differently based on gradient and intensity variations, improving feature extraction and analysis.
