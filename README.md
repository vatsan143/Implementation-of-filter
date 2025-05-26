# Implementation-of-filter

## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.

### Step2
Convert the image from BGR to RGB.

### Step3
Apply the required filters for the image separately.

### Step4
Plot the original and filtered image by using matplotlib.pyplot.

### Step5
End the program.

## Program:
### Developed By: Srivatsan G
### Register Number: 212223230216
</br>

### 1. Smoothing Filters

#### i) Using Averaging Filter

```Python
import cv2
import numpy as np
import matplotlib.pyplot as 
image = cv2.imread('pcb.jpg', cv2.IMREAD_GRAYSCALE)
kernel = np.ones((4, 4), np.float32) / 9
averaged_image = cv2.filter2D(image, -1, kernel)
plt.imshow(averaged_image, cmap='gray')
plt.title("Averaging Filter")
plt.axis('off')
plt.show()
```

#### ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```

#### iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```

#### iv) Using Median Filter
```Python
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```

### 2. Sharpening Filters

#### i) Using Laplacian Linear Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```

#### ii) Using Laplacian Operator
```Python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```

## OUTPUT:

### Original image

![image](https://github.com/user-attachments/assets/bacb1892-afad-4f5d-9ca2-159c50d4c3d7)

### 1. Smoothing Filters
</br>

#### i) Using Averaging Filter

![image](https://github.com/user-attachments/assets/5bcba7d1-92d0-4d7c-b373-6358763c5e8e)

#### ii) Using Weighted Averaging Filter

![image](https://github.com/user-attachments/assets/401534c5-4d9e-44af-bbda-7e5bb30a538c)

#### iii) Using Gaussian Filter

![image](https://github.com/user-attachments/assets/44542f8e-6171-40bd-af73-ff659c918396)

#### iv) Using Median Filter

![image](https://github.com/user-attachments/assets/600a582a-cd7a-4993-873f-8e1ab3ca958e)

### 2. Sharpening Filters
</br>

#### i) Using Laplacian Kernal

![image](https://github.com/user-attachments/assets/de467b1a-7452-461f-9bca-9ba3142c6563)

#### ii) Using Laplacian Operator

![image](https://github.com/user-attachments/assets/6682e542-e388-477a-a7e8-c25dd21d2a50)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
