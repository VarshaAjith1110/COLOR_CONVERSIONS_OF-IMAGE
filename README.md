# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By:
### Register Number: 


## Output:

### i) Read and display the image
```
import cv2
image=cv2.imread('vn.jpg',1)
image=cv2.resize(image,(400,300))
cv2.imshow('window',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![Screenshot 2024-02-22 082528](https://github.com/VarshaAjith1110/COLOR_CONVERSIONS_OF-IMAGE/assets/94222288/461a3195-31ca-4774-93b6-b644001f14d3)


### ii)Write the image
```
import cv2
image=cv2.imread('vn.jpg',0)
image=cv2.resize(image,(400,300))
cv2.imwrite('new1.png',image)
```
![image](https://github.com/VarshaAjith1110/COLOR_CONVERSIONS_OF-IMAGE/assets/94222288/5eae6982-d795-4697-bc1a-6d38bf0b1e39)


### iii)Shape of the Image

```
import cv2
image=cv2.imread('vn.jpg',1)
print(image.shape)
```
![image](https://github.com/VarshaAjith1110/COLOR_CONVERSIONS_OF-IMAGE/assets/94222288/900b715a-9043-4cf1-8aba-95c2bd02c339)
![Screenshot 2024-02-22 082806](https://github.com/VarshaAjith1110/COLOR_CONVERSIONS_OF-IMAGE/assets/94222288/d610ce3f-34b6-4043-bba0-933152216d1e)


### iv)Access rows and columns
```
import random
import cv2
image=cv2.imread('vn.jpg',1)
image=cv2.resize(image,(400,400))
for i in range (150,200):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255),random.randint(0,255),random.randint(0,255)] 
cv2.imshow('WINDOW2',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-02-22 082704](https://github.com/VarshaAjith1110/COLOR_CONVERSIONS_OF-IMAGE/assets/94222288/399d4529-1d2a-44d6-ad7e-76b9aed483b6)
### v)Cut and paste portion of image
```
import cv2
image=cv2.imread('vn.jpg',1)
image=cv2.resize(image,(400,400))
tag =image[150:200,110:160]
image[110:160,150:200] = tag
cv2.imshow('WINDOW3',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-02-22 082806](https://github.com/VarshaAjith1110/COLOR_CONVERSIONS_OF-IMAGE/assets/94222288/d610ce3f-34b6-4043-bba0-933152216d1e)

### vi) BGR and RGB to HSV and GRAY
```
import cv2
img = cv2.imread('vn.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-02-22 082939](https://github.com/VarshaAjith1110/COLOR_CONVERSIONS_OF-IMAGE/assets/94222288/f8065f80-69d0-477f-9acb-4ea72b0de4a8)

### vii) HSV to RGB and BGR
```
import cv2
img = cv2.imread('vn.jpg')
img = cv2.resize(img,(300,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/VarshaAjith1110/COLOR_CONVERSIONS_OF-IMAGE/assets/94222288/69b6555f-3f87-4e3b-ba0a-439950caf5f5)

### viii) RGB and BGR to YCrCb
```
import cv2
img = cv2.imread('vn.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/VarshaAjith1110/COLOR_CONVERSIONS_OF-IMAGE/assets/94222288/049f2621-5752-40a8-87f7-881e9e5e22da)

### ix) Split and merge RGB Image


### x) Split and merge HSV Image
<br>
<br>




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







