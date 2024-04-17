
# Implementation-of-Erosion-and-Dilation

## Aim

To implement Erosion and Dilation using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

   
## Algorithm:

### Step1:

Import necessary packages

### Step2:

Create an empty window and add text to it

### Step3:

create a structuring element

### Step4:

Do the operation

### Step5:

Show the output image

### Name: SANJAY T
### Register Number: 212222110039
 
## Program:

``` Python
import cv2
import numpy as np
from matplotlib import pyplot as plt
```

```py
#to read the color image
input_image_path='dip09.jpg'
color_image=cv2.imread(input_image_path)
```
```py
#convert the color image to grayscale
gray_image=cv2.cvtColor(color_image,cv2.COLOR_BGR2GRAY)
```
```py
#perform edge detection using Canny
edges=cv2.Canny(gray_image,100,200)
```
```py
#define the kernel size for erosion and dilation
kernel_size=5
kernel=np.ones((kernel_size,kernel_size),np.uint8)
```
```py
#perform erosion
erosion=cv2.erode(edges,kernel,iterations=1)

#perform dilation
dilation=cv2.dilate(edges,kernel,iterations=1)
```
```py

#Display original image
plt.imshow(cv2.cvtColor(color_image,cv2.COLOR_BGR2RGB))
plt.title('Original Color Image')
plt.axis('on')
```
```py
#display all images
plt.figure(figsize=(7,7))

plt.subplot(2,2,1)
plt.imshow(gray_image,cmap='gray')
plt.title('Black and White Image')
plt.axis('on')

plt.subplot(2,2,2)
plt.imshow(edges,cmap='gray')
plt.title('Edge Segmentation')
plt.axis('on')

plt.subplot(2,2,3)
plt.imshow(erosion,cmap='gray')
plt.title('Erosion')
plt.axis('on')

plt.subplot(2,2,4)
plt.imshow(dilation,cmap='gray')
plt.title('Dilation')
plt.axis('on')

plt.show()
```
## Output:

### Display the input Image

![image](https://github.com/sanjaythiyagarajan/erosion-dilation/assets/119409242/c7265b01-e014-48ad-997b-3f5ec4eb92d9)


### Display the Eroded Image

![image](https://github.com/sanjaythiyagarajan/erosion-dilation/assets/119409242/84eebf5a-7eb8-48d1-a2ce-952dc206cb49)


### Display the Dilated Image

![image](https://github.com/sanjaythiyagarajan/erosion-dilation/assets/119409242/46cdb16b-f5a2-41f0-85f8-ae5744d8bebe)


### Full output

![image](https://github.com/sanjaythiyagarajan/erosion-dilation/assets/119409242/04f25ffe-f0cd-4f0f-aa92-0faaf18a2b4c)



## Result

### Thus the generated text image is eroded and dilated using python and OpenCV.
