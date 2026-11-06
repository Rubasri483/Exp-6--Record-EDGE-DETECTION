# EXP. 6 – EDGE DETECTION USING OPENCV

## NAME:  Rubasri R
## REG NO: 212224240139

## Aim

To implement different edge detection techniques using OpenCV and Python to identify edges and boundaries in an image.

## Software Requirements

- Python
- Anaconda
- Jupyter Notebook
- OpenCV
- NumPy
- Matplotlib

## Edge Detection Techniques

1. Sobel Edge Detection
2. Laplacian Edge Detection
3. Canny Edge Detection

## Algorithm

1. Import the required libraries: OpenCV, NumPy, and Matplotlib.
2. Read the input image using `cv2.imread()`.
3. Convert the input image into grayscale.
4. Display the original image.
5. Apply Sobel edge detection in horizontal and vertical directions.
6. Combine both Sobel gradients using `cv2.magnitude()`.
7. Apply Laplacian edge detection using `cv2.Laplacian()`.
8. Apply Canny edge detection using `cv2.Canny()`.
9. Display all the edge-detected images separately.
10. Compare the results of different edge detection techniques.

## Implementation

### 1. Import Libraries

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

### 2. Read and Convert the Image

```python
image = cv2.imread('Image.png')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
```

### 3. Display Original Image

```python
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```

## OUTPUT:
<img width="348" height="413" alt="Screenshot 2026-10-30 160311" src="https://github.com/user-attachments/assets/3d9bc175-f22d-4fff-92c6-281bce57922f" />

### 4. Sobel Edge Detection

```python
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)

sobel_combined = cv2.magnitude(sobel_x, sobel_y)

plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```

## OUTPUT:
<img width="363" height="416" alt="image" src="https://github.com/user-attachments/assets/4dbdfc09-9921-4198-a57b-ef81c22142a2" />


### 5. Laplacian Edge Detection

```python
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)

plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```

## OUTPUT;
<img width="351" height="422" alt="image" src="https://github.com/user-attachments/assets/cfe86e68-c281-4eed-817f-a660327ddf00" />


### 6. Canny Edge Detection

```python
canny_edges = cv2.Canny(gray_image, 50, 150)

plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```

## Output:
<img width="407" height="419" alt="image" src="https://github.com/user-attachments/assets/f389e552-f508-405a-bc1e-ecab02eec5d8" />

## Result

Thus, Sobel, Laplacian, and Canny edge detection techniques were successfully implemented using OpenCV and Python. Each technique detects image edges differently and helps identify important boundaries and features.
