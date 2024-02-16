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
### Developed By:SRIRAM S S
### Register Number: 212222230150


## Output:

### i) Read and display the image

```python
    import cv2
    image=cv2.imread('Untitled.png',1)
    image=cv2.resize(image,(300,300))
    cv2.imshow('sriram',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
![Screenshot 2024-02-16 082625](https://github.com/sriramss4880/COLOR_CONVERSIONS_OF-IMAGE/assets/120554177/0db8da9c-b367-4aab-8704-79b202e5eeda)

![Screenshot 2024-02-16 082615](https://github.com/sriramss4880/COLOR_CONVERSIONS_OF-IMAGE/assets/120554177/c2a64361-6047-480a-b0f2-0834458e3215)

### ii)Write the image

```python
    import cv2
    image=cv2.imread('Untitled.png',0)
    cv2.imwrite('demos.jpg',image)
```
![Screenshot 2024-02-16 082726](https://github.com/sriramss4880/COLOR_CONVERSIONS_OF-IMAGE/assets/120554177/762d982f-1cfd-4db4-a068-ebf74b6ee765)

### iii)Shape of the Image

```python
    import cv2
    image=cv2.imread('Untitled.png',1)
    print(image.shape)
```
![Screenshot 2024-02-16 082801](https://github.com/sriramss4880/COLOR_CONVERSIONS_OF-IMAGE/assets/120554177/beac8afe-57ac-4caf-84f2-197f951a5ff4)


### iv)Access rows and columns

```python
import random
import cv2
image=cv2.imread('Untitled.png',1)
image=cv2.resize(image,(500,500))
for i in range (250,500):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
cv2.imshow('part image',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-02-16 082939](https://github.com/sriramss4880/COLOR_CONVERSIONS_OF-IMAGE/assets/120554177/5a6d2744-a649-4ef3-a92e-4765283bf97c)

![Screenshot 2024-02-16 082927](https://github.com/sriramss4880/COLOR_CONVERSIONS_OF-IMAGE/assets/120554177/58fff957-da61-43e8-ba4d-1ed4b9848a01)


### v)Cut and paste portion of image

```python
  import cv2
  image=cv2.imread('Untitled.png',1)
  image=cv2.resize(image,(300,300))
  tag =image[150:200,110:160]
  image[110:160,150:200] = tag
  cv2.imshow('image1',image)
  cv2.waitKey(0)
  cv2.destroyAllWindows()
```

![Screenshot 2024-02-16 083036](https://github.com/sriramss4880/COLOR_CONVERSIONS_OF-IMAGE/assets/120554177/24d9e0c2-9118-47a3-93c3-0f14b8aaf009)

![Screenshot 2024-02-16 083027](https://github.com/sriramss4880/COLOR_CONVERSIONS_OF-IMAGE/assets/120554177/3e977ab4-9158-4975-9aaa-32b04d6bd0b8)

### vi) BGR and RGB to HSV and GRAY

```python
import cv2
img = cv2.imread('Untitled.png',1)
img = cv2.resize(img,(200,200))
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

![Screenshot 2024-02-16 083155](https://github.com/sriramss4880/COLOR_CONVERSIONS_OF-IMAGE/assets/120554177/be14f002-ee09-4d7d-b10d-8d2c34273a01)

![Screenshot 2024-02-16 083135](https://github.com/sriramss4880/COLOR_CONVERSIONS_OF-IMAGE/assets/120554177/35f7b323-96a2-4845-ac98-1e69c014cf4d)


### vii) HSV to RGB and BGR

```python
import cv2
img = cv2.imread('Untitled.png')
img = cv2.resize(img,(200,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-02-16 083259](https://github.com/sriramss4880/COLOR_CONVERSIONS_OF-IMAGE/assets/120554177/bb85995a-6af3-48d8-8772-0ef41dad49cd)

![Screenshot 2024-02-16 083245](https://github.com/sriramss4880/COLOR_CONVERSIONS_OF-IMAGE/assets/120554177/0c8e1680-29c7-4df7-90a7-d4d1fe983fce)


### viii) RGB and BGR to YCrCb

```python
import cv2
img = cv2.imread('Untitled.png')
img = cv2.resize(img,(200,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-02-16 083359](https://github.com/sriramss4880/COLOR_CONVERSIONS_OF-IMAGE/assets/120554177/f9df903f-e216-48dd-b0f1-3a36f5fe7c5b)

![Screenshot 2024-02-16 083346](https://github.com/sriramss4880/COLOR_CONVERSIONS_OF-IMAGE/assets/120554177/e656cd82-764b-4b3f-aadd-c9dcb782480a)


### ix) Split and merge RGB Image
```python
import cv2
img = cv2.imread('Untitled.png',1)
img = cv2.resize(img,(200,200))

R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]

cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)

merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-02-16 083452](https://github.com/sriramss4880/COLOR_CONVERSIONS_OF-IMAGE/assets/120554177/4224d797-94ef-4e6f-8ae8-9993180d0247)

![Screenshot 2024-02-16 083442](https://github.com/sriramss4880/COLOR_CONVERSIONS_OF-IMAGE/assets/120554177/3a69c081-3dc1-4fae-9dd7-5cc51cb6e674)

### x) Split and merge HSV Image
```python
import cv2
img = cv2.imread("Untitled.png",1)
img = cv2.resize(img,(200,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)

H,S,V=cv2.split(img)

cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)

merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/sriramss4880/COLOR_CONVERSIONS_OF-IMAGE/assets/120554177/7a252a56-6f86-4a9e-baf6-0d025e434c04)

![Screenshot 2024-02-16 083612](https://github.com/sriramss4880/COLOR_CONVERSIONS_OF-IMAGE/assets/120554177/3bd1aa12-8f03-49e5-8a68-5d4c35d3b1e3)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.








