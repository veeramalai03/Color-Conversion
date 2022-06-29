## Ex no: 3
## Date: 11/04/2022
# <p align="center">Color Conversion</p>
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
<br>Import cv2 and save and image as filename.jpg

### Step2:
<br>Use imread(filename, flags) to read the file.

### Step3:
<br>Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space toanother

### Step4:
<br>Split and merge the image using cv2.split and cv2.merge commands

### Step5:
<br>End the program and close the output image windows.

## Program:
```python
# Developed By: VEERAMALAI S
# Register Number: 212220230056
# i) Convert BGR and RGB to HSV and GRAY
import cv2
color_image = cv2.imread('cap vs tony.jpg')
cv2.imshow('Original image',color_image)
hsv_image = cv2.cvtColor(color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV' ,hsv_image )
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_RGB2GRAY)cv2.imshow('RGB2GRAY', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()
# ii)Convert HSV to RGB and BGR
import cv2
color_image = cv2.imread('cap vs tony.jpg')
cv2.imshow('Original image', color_image)
hsv_image = cv2.cvtColor(color_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB' ,hsv_image )
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()
# iii)Convert RGB and BGR to YCrCb
import cv2
color_image = cv2.imread('cap vs tony.jpg')
cv2.imshow('Original image',color_image)
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_RGB2YCrCb)cv2.imshow('RGB2YCrCb', gray_image1)
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_BGR2YCrCb)cv2.imshow('BGR2YCrCb', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()
# iv)Split and Merge RGB Image
import cv2
image = cv2.imread('cap vs tony.jpg')
blue=image[:,:,0]
green=image[:,:,1]
red=image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
Merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',Merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()
# v) Split and merge HSV Image
Output:
i) BGR and RGB to HSV and GRAY
import cv2
image = cv2.imread('cap vs tony.jpg')
hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue-Image',h)
cv2.imshow('Saturation-Image',s)
cv2.imshow('Gray-Image',v)
Merged_HSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()

```
## Output:
### i) BGR and RGB to HSV and GRAY
<br>![2022-04-11 (3)](https://user-images.githubusercontent.com/75234790/162795504-fb7ebdfb-56f2-4d84-9eff-72d481144f5a.png)
<br>![2022-04-11 (4)](https://user-images.githubusercontent.com/75234790/162795552-d8e99136-cbf7-4bbe-b2ac-480b3b3ea40c.png)
<br>![2022-04-11 (5)](https://user-images.githubusercontent.com/75234790/162795599-b99ca684-934c-484f-a2df-33f69ff37850.png)


### ii) HSV to RGB and BGR
<br>![2022-04-11 (7)](https://user-images.githubusercontent.com/75234790/162795696-8da9678c-3613-4c90-a541-7155b4832f64.png)

<br>![2022-04-11 (8)](https://user-images.githubusercontent.com/75234790/162795716-664d0ced-1fe0-4151-b123-5041b92c9620.png)


### iii) RGB and BGR to YCrCb
<br>![2022-04-11 (9)](https://user-images.githubusercontent.com/75234790/162795744-922444df-9c78-467f-89a8-dee4379a6ab9.png)

<br>![2022-04-11 (10)](https://user-images.githubusercontent.com/75234790/162795758-5922318c-c2f6-4820-bba1-58e23ac699fc.png)


### iv) Split and merge RGB Image
<br>![2022-04-11 (11)](https://user-images.githubusercontent.com/75234790/162795913-e3df0149-10e6-4510-babb-9b1ab4bd3f4a.png)

<br>![2022-04-11 (12)](https://user-images.githubusercontent.com/75234790/162795923-00f80930-657e-403c-a791-d3f4c3683b29.png)

<br>![2022-04-11 (13)](https://user-images.githubusercontent.com/75234790/162795936-3e5931ca-dd1a-4eeb-9bde-c8766393ecf0.png)


### v) Split and merge HSV Image
<br>![2022-04-11 (14)](https://user-images.githubusercontent.com/75234790/162795979-d433c937-7276-469c-aa53-ab55a960654b.png)

<br>![2022-04-11 (15)](https://user-images.githubusercontent.com/75234790/162795992-5f6a33e2-64c2-4ca4-b76a-32c55512b117.png)

<br>![2022-04-11 (16)](https://user-images.githubusercontent.com/75234790/162796011-30f90df9-e182-43ea-8cea-b176bd739475.png)

<br>![2022-04-11 (17)](https://user-images.githubusercontent.com/75234790/162796021-a6d2a81f-ea87-4e02-aebe-ee1f5a7d698d.png)



## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
