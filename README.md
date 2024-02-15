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

##  Program:

```
### Developed By: ABINAYA S
### Register Number: 212222230002
```

### i) Read and display the image
```Python
    import cv2
    image=cv2.imread('Abinaya.jpeg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('Abinaya',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
  </td>
  <td>
    
#### OUTPUT:

![img1](https://github.com/abinayasangeetha/COLOR_CONVERSIONS_OF-IMAGE/assets/119393675/cd1906f2-101c-4057-88bb-d173973a191c)
</td>
</tr>



<tr>
  <td width=50%>

### ii)Write the image
```Python
    import cv2
    image=cv2.imread('Abinaya.jpeg',0)
    cv2.imwrite('apple.jpeg',image)
```
  </td>
  <td>

#### OUTPUT:

![img2](https://github.com/abinayasangeetha/COLOR_CONVERSIONS_OF-IMAGE/assets/119393675/d97708f5-e4fe-4fde-84cb-46270ab68a94)

</td>
</tr> 
<tr> 
  <td width=50%>



### iii)Shape of the Image
```Python
    import cv2
    image=cv2.imread('Abinaya.jpeg',1)
    print(image.shape)
```
  </td> 
  <td>

#### OUTPUT:
![img3](https://github.com/abinayasangeetha/COLOR_CONVERSIONS_OF-IMAGE/assets/119393675/2a88bfb5-fa9f-4b04-9b99-2bdf87689edf)

  </td>
  </tr> 
  <tr>
    <td>


      
### iv)Access rows and columns
```Python
     import random
     import cv2
     image=cv2.imread('Abinaya.jpeg',1)
     image=cv2.resize(image,(400,400))
     for i in range (150,200):
       for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
     cv2.imshow('part image',image)
     cv2.waitKey(0)
     cv2.destroyAllWindows()
```
  </td>
  <td width="50%">
 
      
#### OUTPUT:
![img4](https://github.com/abinayasangeetha/COLOR_CONVERSIONS_OF-IMAGE/assets/119393675/d2b764ac-f593-45a4-80aa-540157d259a5)



 </td>
 </tr>
 <tr>
  <td width=50%>

### v)Cut and paste portion of image
```Python
     import cv2
     image=cv2.imread('Abinaya.jpeg',1)
     image=cv2.resize(image,(400,400))
     tag =image[150:200,110:160]
     image[110:160,150:200] = tag
     cv2.imshow('partimage1',image)
     cv2.waitKey(0)
     cv2.destroyAllWindows()
```
  </td>
  <td>

#### OUTPUT:
![img5](https://github.com/abinayasangeetha/COLOR_CONVERSIONS_OF-IMAGE/assets/119393675/66ba6ccd-fb1a-48d4-87b8-1815edb39d81)


 </td>
 </tr>
</table>


### vi) BGR and RGB to HSV and GRAY
```Python
    import cv2
    img = cv2.imread('Abinaya.jpeg',1)
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
#### OUTPUT:
![img6](https://github.com/abinayasangeetha/COLOR_CONVERSIONS_OF-IMAGE/assets/119393675/940e70bf-9ce7-4444-93e2-dd5ea2376b54)


### vii) HSV to RGB and BGR
```Python
import cv2
img = cv2.imread('Abinaya.jpeg')
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
#### OUTPUT:
![img7](https://github.com/abinayasangeetha/COLOR_CONVERSIONS_OF-IMAGE/assets/119393675/7361d544-982a-439a-a140-15218d9df6ae)


### viii) RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread('Abinaya.jpeg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
#### OUTPUT:
![img8](https://github.com/abinayasangeetha/COLOR_CONVERSIONS_OF-IMAGE/assets/119393675/70a365e7-2b12-4b8f-b432-3ee3964feeb5)


### ix) Split and merge RGB Image
```Python
import cv2
img = cv2.imread('Abinaya.jpeg',1)
img = cv2.resize(img,(300,200))

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
#### OUTPUT:
![img9](https://github.com/abinayasangeetha/COLOR_CONVERSIONS_OF-IMAGE/assets/119393675/9b559e3a-cfc5-456a-8684-97b17b224c1d)


### x) Split and merge HSV Image
```Python
import cv2
img = cv2.imread("Abinaya.jpeg",1)
img = cv2.resize(img,(300,200))
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
#### OUTPUT:

![img10](https://github.com/abinayasangeetha/COLOR_CONVERSIONS_OF-IMAGE/assets/119393675/8dbbc44d-6f5c-40a6-b0cf-32d65619b8ad)




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







