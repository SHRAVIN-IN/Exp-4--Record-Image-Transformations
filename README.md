# Geometric Transformations Using OpenCV

---

## Aim

To write a Python program using OpenCV to perform various geometric transformations on an image.

The program performs the following operations:

- Image Translation  
- Image Scaling (Resizing)  
- Image Shearing  
- Image Reflection (Flipping)  
- Image Rotation  

---

##  Software Used

- Anaconda – Python 3.7  
- Jupyter Notebook / VS Code  
- OpenCV (`cv2`)  
- NumPy  
- Matplotlib  

---

##  Algorithm

### Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:
Read the input image in color mode.

### Step 3: Image Translation
- Create a translation matrix to shift the image  
- Move the image 50 pixels to the right and 80 pixels down  
- Apply transformation using `cv2.warpAffine()`  
- Display original and translated images  

### Step 4: Image Scaling
- Resize the image to 0.5× (downscale)  
- Resize the image to 2× (upscale)  
- Use `cv2.resize()`  
- Display original, downscaled, and upscaled images  

### Step 5: Image Shearing
- Create transformation matrices for:
  - Horizontal shearing  
  - Vertical shearing  
- Apply transformations using `cv2.warpAffine()`  
- Display original and sheared images  

### Step 6: Image Reflection
- Perform flipping using `cv2.flip()`:
  - Horizontal reflection  
  - Vertical reflection  
  - Both axes  
- Display all reflected images  

### Step 7: Image Rotation
- Create rotation matrices for:
  - 45° rotation  
  - 90° rotation  
- Use `cv2.getRotationMatrix2D()` and `cv2.warpAffine()`  
- Display original and rotated images  

---

##  Program
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('spider.png')

# Display original image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis('off')
plt.show()

# Image Translation
tx, ty = 100, 50
M_translation = np.float32([[1, 0, tx],
                            [0, 1, ty]])
translated_image = cv2.warpAffine(
    image, M_translation, (image.shape[1], image.shape[0])
)

plt.imshow(cv2.cvtColor(translated_image, cv2.COLOR_BGR2RGB))
plt.title("Translated Image")
plt.axis('off')
plt.show()

# Image Scaling
fx, fy = 5.0, 2.0
scaled_image = cv2.resize(
    image, None, fx=fx, fy=fy,
    interpolation=cv2.INTER_LINEAR
)

plt.imshow(cv2.cvtColor(scaled_image, cv2.COLOR_BGR2RGB))
plt.title("Scaled Image")
plt.axis('off')
plt.show()

# Image Shearing
shear_matrix = np.float32([[1, 0.5, 0],
                           [0.5, 1, 0]])

sheared_image = cv2.warpAffine(
    image, shear_matrix, (image.shape[1], image.shape[0])
)

plt.imshow(cv2.cvtColor(sheared_image, cv2.COLOR_BGR2RGB))
plt.title("Sheared Image")
plt.axis('off')
plt.show()

# Image Reflection
reflected_image = cv2.flip(image, 2)

plt.imshow(cv2.cvtColor(reflected_image, cv2.COLOR_BGR2RGB))
plt.title("Reflected Image")
plt.axis('off')
plt.show()

# Image Rotation
(height, width) = image.shape[:2]
angle = 45
center = (width // 2, height // 2)

M_rotation = cv2.getRotationMatrix2D(center, angle, 1)
rotated_image = cv2.warpAffine(
    image, M_rotation, (width, height)
)

plt.imshow(cv2.cvtColor(rotated_image, cv2.COLOR_BGR2RGB))
plt.title("Rotated Image")
plt.axis('off')
plt.show()

# Image Cropping
x, y, w, h = 100, 100, 200, 150
cropped_image = image[y:y+h, x:x+w]

plt.imshow(cv2.cvtColor(cropped_image, cv2.COLOR_BGR2RGB))
plt.title("Cropped Image")
plt.axis('off')
plt.show()
```
### Developed By:
**Name:** S. Jana Shravin

### Register No:
212224243003  

---

##  Output
<img width="512" height="409" alt="9fe058d0-00d7-4f97-9de0-245876085626" src="https://github.com/user-attachments/assets/bbfcccef-facc-46f2-b4c7-a1878dac5776" />
<img width="515" height="370" alt="bf79a143-2223-452d-b9ea-51560b1885b7" src="https://github.com/user-attachments/assets/be5c383a-dc6a-4fa3-b817-f455d39b1889" />
<img width="515" height="370" alt="bee1b9f2-a38a-4c1d-bcaf-5135a08991d9" src="https://github.com/user-attachments/assets/7ff2d806-2b12-429a-a3f5-f4ff15c42c61" />
<img width="515" height="370" alt="935426fc-8c7f-4c81-ae88-8588d1821406" src="https://github.com/user-attachments/assets/cdb178fa-8993-41d4-a853-2c0a0a9021cd" />
<img width="515" height="172" alt="04c168b2-84d6-40be-bfef-6b9a3a52ed22" src="https://github.com/user-attachments/assets/533d4220-3b77-4ffc-aa87-7c5651018127" />
<img width="515" height="370" alt="8590b3fd-184a-45d0-9ea2-9f909e9760d8" src="https://github.com/user-attachments/assets/c8f9eada-dd63-410f-a9f5-26c81f31603d" />
<img width="515" height="370" alt="73ee21e2-e7fa-4e30-b243-e95b8106437c" src="https://github.com/user-attachments/assets/2f920c44-f12d-45b5-9c21-4517707f97b1" />

### Image Translation
- Original image is displayed  
- Translated image (shifted right and down) is displayed  

### Image Scaling
- Original image is displayed  
- Downscaled image (0.5×) is displayed  
- Upscaled image (2×) is displayed  

### Image Shearing
- Original image is displayed  
- Horizontally sheared image is displayed  
- Vertically sheared image is displayed  

### Image Reflection
- Original image is displayed  
- Horizontally flipped image is displayed  
- Vertically flipped image is displayed  
- Both-axis flipped image is displayed  

### Image Rotation
- Original image is displayed  
- 45° rotated image is displayed  
- 90° rotated image is displayed  

---

##  Result

Thus, various geometric transformations such as translation, scaling, shearing, reflection, and rotation are successfully performed using OpenCV. These transformations demonstrate how images can be spatially manipulated for different computer vision applications.
