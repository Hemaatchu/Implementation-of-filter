# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
</br>
Import the required libraries.
</br> 

### Step2
</br>

Convert the image from BGR to RGB.
</br> 

### Step3
</br>
Apply the required filters for the image separately.
</br> 

### Step4
</br>
Plot the original and filtered image by using matplotlib.pyplot.
</br> 

### Step5
</br>
End the program.
</br> 



## Program:
### Developed By   :Hemavathy S
### Register Number:212223230076

### 1. Smoothing Filters
i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("nature.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()
```
ii) Using Weighted Averaging Filter
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()

```
iii) Using Gaussian Filter
```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```
iv)Using Median Filter
```
median=cv2.medianBlur(image2,13)
plt.title("Median Blur")
plt.axis('off')
plt.show()

```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()

```
ii) Using Laplacian Operator
```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()

```

## OUTPUT:
### 1. Smoothing Filters

i) Using Averaging Filter
<img width="1208" height="385" alt="image" src="https://github.com/user-attachments/assets/d1f7acb2-18bd-4e54-a75d-b2abc620b573" />


ii)Using Weighted Averaging Filter
<img width="771" height="564" alt="image" src="https://github.com/user-attachments/assets/56f0ba59-dcdb-413e-9a67-cc59f6edf580" />


iii)Using Gaussian Filter
<img width="826" height="560" alt="image" src="https://github.com/user-attachments/assets/4be749a1-ed14-4cc5-83b6-edea589f4bac" />


iv) Using Median Filter
<img width="785" height="549" alt="image" src="https://github.com/user-attachments/assets/ab9dc1fa-0efc-47a2-8633-fff7a6e4caf8" />


### 2. Sharpening Filters

i) Using Laplacian Kernal


<img width="782" height="544" alt="image" src="https://github.com/user-attachments/assets/0be8dcd0-c594-4846-95d2-17a8c302f337" />


ii) Using Laplacian Operator

<img width="786" height="534" alt="image" src="https://github.com/user-attachments/assets/20422148-e392-43e8-bfd3-5e83379ff461" />

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
