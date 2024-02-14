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
### Step1: Choose an image and save it as a filename.jpg ,
### Step2: Use imread(filename, flags) to read the file.
### Step3: Use imshow(window_name, image) to display the image.
### Step4: Use imwrite(filename, image) to write the image.
### Step5: End the program and close the output image windows.
### Step6: Convert BGR and RGB to HSV and GRAY
### Step7: Convert HSV to RGB and BGR
### Step8: Convert RGB and BGR to YCrCb
### Step9: Split and Merge RGB Image
### Step10: Split and merge HSV Image

##### Program:
```
### Developed By: Ragavendran A
### Register Number: 212222230114
```
<table>
  <tr>
    <td width=50%>

### i) Read and display the image
```Python
    import cv2
    image=cv2.imread('pic1.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('RAGAVENDRAN A',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
``` 
  </td>
  <td>

### OUTPUT:
![out1](https://github.com/ragavanayyadurai/COLOR_CONVERSIONS_OF-IMAGE/assets/118749557/2de219cc-7bc5-4a48-99e0-d53bfbe79cb4)

  </td>
  </tr>

   <tr>
    <td width=50%>

### ii)Write the image
```Python
    import cv2
    image=cv2.imread('pic1.jpg',0)
    cv2.imwrite('demos.jpg',image)
```
  </td>
  <td>

### OUTPUT:

![Screenshot 2024-02-14 210503](https://github.com/ragavanayyadurai/COLOR_CONVERSIONS_OF-IMAGE/assets/118749557/358c4717-b16f-4194-9356-362c2d6eab8e)
  </td>
  </tr>
  <tr>
    <td width=50%>

### iii)Shape of the Image
```Python
    import cv2
    image=cv2.imread('pic1.jpg',1)
    print(image.shape)
```
  </td>
  <td>

### OUTPUT:
![Screenshot 2024-02-14 210709](https://github.com/ragavanayyadurai/COLOR_CONVERSIONS_OF-IMAGE/assets/118749557/96fc0e40-f8a0-45c2-ba4d-f05e5618a7fd)
  </td>
  </tr>
  <tr>
    <td>
      
### iv)Access rows and columns
```Python
    import random
    import cv2
    image=cv2.imread('pic1.jpg',1)
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

### OUTPUT:
![out2](https://github.com/ragavanayyadurai/COLOR_CONVERSIONS_OF-IMAGE/assets/118749557/e1a6fab6-f572-4fe0-857d-fd703275eebf)

  </td>
  </tr>
  <tr>
    <td width=50%>
      
### v)Cut and paste portion of image

 ```Python
    import cv2
    image=cv2.imread('pic1.jpg',1)
    image=cv2.resize(image,(400,400))
    tag =image[130:200,110:190]
    image[110:180,120:200] = tag
    cv2.imshow('partimage1',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
  </td>
  <td>
    
### OUTPUT:
![out3](https://github.com/ragavanayyadurai/COLOR_CONVERSIONS_OF-IMAGE/assets/118749557/c029cd03-75f0-4965-889f-64506e0adccc)

  </td>
  </tr>
</table>

### vi) BGR and RGB to HSV and GRAY
```Python
import cv2
img = cv2.imread('pic1.jpg',1)
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

### OUTPUT:
![out4 1](https://github.com/ragavanayyadurai/COLOR_CONVERSIONS_OF-IMAGE/assets/118749557/0bd75df7-28d7-4d35-ad6b-3d220a9e5a81)
![out4 2](https://github.com/ragavanayyadurai/COLOR_CONVERSIONS_OF-IMAGE/assets/118749557/7ab6f9ef-1305-40b4-8ecb-5b7da578e370)
![out4 3](https://github.com/ragavanayyadurai/COLOR_CONVERSIONS_OF-IMAGE/assets/118749557/8efa3f90-6a55-42f3-87d4-d48d94858afd)
![out4 4](https://github.com/ragavanayyadurai/COLOR_CONVERSIONS_OF-IMAGE/assets/118749557/c3f8c414-ad60-4190-ac88-3d4ffcb0bae0)
![out4 5](https://github.com/ragavanayyadurai/COLOR_CONVERSIONS_OF-IMAGE/assets/118749557/45be81fe-a1f2-4d75-b1bb-22f65f9f3a36)

### vii) HSV to RGB and BGR
```Python
import cv2
img = cv2.imread('pic1.jpg')
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

### OUTPUT:
![out5 1](https://github.com/ragavanayyadurai/COLOR_CONVERSIONS_OF-IMAGE/assets/118749557/9649ba73-5faa-41c6-8891-77a91b53910d)
![out5 2](https://github.com/ragavanayyadurai/COLOR_CONVERSIONS_OF-IMAGE/assets/118749557/c9ea545f-d634-4572-98cd-abc3d6e7f45d)
![out5 3](https://github.com/ragavanayyadurai/COLOR_CONVERSIONS_OF-IMAGE/assets/118749557/bcac712d-438a-4cf0-9fbf-6c7a4e38afba)

### viii) RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread('pic1.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![out6 1](https://github.com/ragavanayyadurai/COLOR_CONVERSIONS_OF-IMAGE/assets/118749557/2bcecedb-b52c-4947-9fde-58ef81e2bcfb)
![out6 2](https://github.com/ragavanayyadurai/COLOR_CONVERSIONS_OF-IMAGE/assets/118749557/56d80788-1815-4ffa-ad3c-0107e53cf2f4)
![out6 3](https://github.com/ragavanayyadurai/COLOR_CONVERSIONS_OF-IMAGE/assets/118749557/8d2a88d8-deaa-4a48-8b89-5bc71c09f364)

### ix) Split and merge RGB Image
```Python
import cv2
img = cv2.imread('pic1.jpg',1)
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

### OUTPUT:
![out7 1](https://github.com/ragavanayyadurai/COLOR_CONVERSIONS_OF-IMAGE/assets/118749557/e7e4f6c2-aa32-459a-9da8-d171031c3579)
![out7 2](https://github.com/ragavanayyadurai/COLOR_CONVERSIONS_OF-IMAGE/assets/118749557/ba160850-0f38-4b95-a885-0e9905e0e4b3)
![out7 3](https://github.com/ragavanayyadurai/COLOR_CONVERSIONS_OF-IMAGE/assets/118749557/b22c7dd6-b49a-4a8a-b9a6-387ff78a61c6)
![out7 4](https://github.com/ragavanayyadurai/COLOR_CONVERSIONS_OF-IMAGE/assets/118749557/d48f67ab-97cb-4397-b9b5-03dcddd14950)

### x) Split and merge HSV Image
```Python
import cv2
img = cv2.imread("pic1.jpg",1)
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

### OUTPUT:
![out8 1](https://github.com/ragavanayyadurai/COLOR_CONVERSIONS_OF-IMAGE/assets/118749557/859218c2-40a9-4eec-906b-21da52a37e39)
![out8 2](https://github.com/ragavanayyadurai/COLOR_CONVERSIONS_OF-IMAGE/assets/118749557/cfe4404f-f318-489d-99a0-a77e147f5743)
![out8 3](https://github.com/ragavanayyadurai/COLOR_CONVERSIONS_OF-IMAGE/assets/118749557/e4bb45d5-a7de-4529-acc1-86da91b70cfe)
![out8 4](https://github.com/ragavanayyadurai/COLOR_CONVERSIONS_OF-IMAGE/assets/118749557/e5437e8a-16b3-4f87-bf85-21ec97c0bac8)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







