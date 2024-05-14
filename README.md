# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm
### Step1:
Import necessary packages

### Step2:
Read the image

### Step3:
If the read image is a color image, convert it into a grayscale image

### Step4:
perform the threshold operation you want to do(global thresholding or adaptive thresholding or otsu's thresholding)

### Step5:
Display the Results

Developed By: Saravanan C
Register No: 212222110041

## Program

## Load the necessary packages
```python
import cv2
```
## Read the Image and convert it to grayscale
```python
img = cv2.imread('cat.jpeg',-1)
cv2.imshow('original_image',img)
cv2.waitKey(0)
cv2.destroyAllWindows
gray =cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('gray_image',gray)
cv2.waitKey(0)
cv2.destroyAllWindows
```
## Use Global thresholding to segment the image
```python
ret,thresh_img1=cv2.threshold(gray,86,255,cv2.THRESH_BINARY)
ret,thresh_img2=cv2.threshold(gray,86,255,cv2.THRESH_BINARY_INV)
ret,thresh_img3=cv2.threshold(gray,86,255,cv2.THRESH_TOZERO)
ret,thresh_img4=cv2.threshold(gray,86,255,cv2.THRESH_TOZERO_INV)
ret,thresh_img5=cv2.threshold(gray,100,255,cv2.THRESH_TRUNC)
```
## Use Adaptive thresholding to segment the image
```python
thresh_img6=cv2.adaptiveThreshold(gray,255,cv2.ADAPTIVE_THRESH_MEAN_C,cv2.THRESH_BINARY,11,2)
thresh_img7=cv2.adaptiveThreshold(gray,255,cv2.ADAPTIVE_THRESH_GAUSSIAN_C,cv2.THRESH_BINARY,11,2)
```

## Use Otsu's method to segment the image 
```python
ret,thresh_img8=cv2.threshold(gray,0,255,cv2.THRESH_BINARY+cv2.THRESH_OTSU)
```


## Display the results
```python
image =[thresh_img1,thresh_img2,thresh_img3,thresh_img4,thresh_img5,thresh_img6,thresh_img7,thresh_img8]
for i in range(0,8):
    cv2.imshow('threshold_image',image[i])
    cv2.waitKey(0)
    cv2.destroyAllWindows

```

## Output


### Original Image
![image](https://github.com/22009011/Thresholdingg/assets/118343461/2f0b4fec-e0b7-422d-842e-99716a0adc52)




### Global Thresholding
![image](https://github.com/22009011/Thresholdingg/assets/118343461/d830e7e0-8677-414a-a480-e5b4462208c1)



![image](https://github.com/22009011/Thresholdingg/assets/118343461/10322dfc-d3a8-4f34-b459-6bdd660537a7)



![image](https://github.com/22009011/Thresholdingg/assets/118343461/096642cf-e138-4f0a-9b46-4cd699b27eda)


![image](https://github.com/22009011/Thresholdingg/assets/118343461/62c0d6e2-9de7-4235-bff2-a346a00bb3ac)


![image](https://github.com/22009011/Thresholdingg/assets/118343461/72763263-c412-4435-bc97-192b58049701)


### Adaptive Thresholding
![image](https://github.com/22009011/Thresholdingg/assets/118343461/c1d3a594-c139-4ca0-a4be-93c75f8fb6c4)


![image](https://github.com/22009011/Thresholdingg/assets/118343461/034160b4-21c3-4476-8f83-8f863e4b9c1a)


### Optimum Global Thesholding using Otsu's Method
![image](https://github.com/22009011/Thresholdingg/assets/118343461/21a786c9-d5a6-49d1-b7f0-43933125bcb6)

## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
