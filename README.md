# IMPLEMENTATION-OF-FILTERSS
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required modules.

### Step2
Convert the image from BGR to RGB.

### Step3
Apply the required filters for the image separately.

### Step4
Plot the original and filtered image by using matplotlib.pyplot
### Step5
End the program.

## Program:
### Developed By   :Adhithya.S
### Register Number: 212222240003


### 1. Smoothing Filters
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("cat.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
```
i) Using Averaging Filter
```Python
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







```
ii) Using Weighted Averaging Filter
```Python

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







```
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(src=image2,ksize=(33,33),sigmaX=0,sigmaY=0)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()








```

iv) Using Median Filter
```Python

median=cv2.medianBlur(src=image2,ksize=11)
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
i) Using Laplacian Kernal
```Python

kernel3=np.array([[0,-1,-1],[2,-4,1],[2,1,0]])
image3=cv2.filter2D(image2,-1,kernel3)
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
ii) Using Laplacian Operator
```Python

new_image=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(new_image)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()








```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
![image](https://github.com/s-adhithya/IMPLEMENTATION-OF-FILTERSS/assets/113497423/828b66ac-09c5-48e8-b804-d41a7be22758)


ii) Using Weighted Averaging Filter
![image](https://github.com/s-adhithya/IMPLEMENTATION-OF-FILTERSS/assets/113497423/49f68a41-a61b-4e05-873f-3b98c8254f04)


iii) Using Gaussian Filter
![image](https://github.com/s-adhithya/IMPLEMENTATION-OF-FILTERSS/assets/113497423/7070959f-b283-4b57-a77f-9f37f0323558)


iv) Using Median Filter
![image](https://github.com/s-adhithya/IMPLEMENTATION-OF-FILTERSS/assets/113497423/6b174716-b4df-4cc4-8f55-5ae8055ae5f0)


### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
![image](https://github.com/s-adhithya/IMPLEMENTATION-OF-FILTERSS/assets/113497423/2e260a48-0329-4b58-8ba9-c173fe654d8c)


ii) Using Laplacian Operator
![image](https://github.com/s-adhithya/IMPLEMENTATION-OF-FILTERSS/assets/113497423/82e54c70-da53-4109-9eb8-9cd77a477d75)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
