# Exp 4 - Geometric Transformations Using OpenCV

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

### Developed By:JANA SHRAVIN S

### Register No: 212224243003

---

##  Output

### Image Translation
- Original image is displayed  
- Translated image (shifted right and down) is displayed  
  <img width="628" height="353" alt="Screenshot 2026-08-20 112144" src="https://github.com/user-attachments/assets/61bd9886-3e8b-421c-93cf-cd4a291115b0" />





### Image Scaling
- Original image is displayed  
- Downscaled image (0.5×) is displayed  
- Upscaled image (2×) is displayed  


<img width="629" height="385" alt="Screenshot 2026-08-20 112249" src="https://github.com/user-attachments/assets/4a01f0a3-953f-480b-9acb-0dbf225f7e48" />



### Image Shearing
- Original image is displayed  
- Horizontally sheared image is displayed  
- Vertically sheared image is displayed  

<img width="622" height="198" alt="Screenshot 2026-08-20 112359" src="https://github.com/user-attachments/assets/f6005826-57ba-4cb2-9947-aa00024fdbf6" />




### Image Reflection
- Original image is displayed  
- Horizontally flipped image is displayed  
- Vertically flipped image is displayed  
- Both-axis flipped image is displayed  

<img width="631" height="392" alt="Screenshot 2026-08-20 112513" src="https://github.com/user-attachments/assets/2189c057-7b16-4960-b5bb-c49f205252b5" />




### Image Rotation
- Original image is displayed  
- 45° rotated image is displayed  
- 90° rotated image is displayed  
<img width="674" height="397" alt="Screenshot 2026-08-20 112601" src="https://github.com/user-attachments/assets/d897eb63-0845-443d-a991-0d84613ecbfd" />




---

##  Result

Thus, various geometric transformations such as translation, scaling, shearing, reflection, and rotation are successfully performed using OpenCV. These transformations demonstrate how images can be spatially manipulated for different computer vision applications.
