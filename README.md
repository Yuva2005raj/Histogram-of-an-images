# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By: YUVARAJ B
# Register Number: 212222230182
import cv2
import matplotlib.pyplot as plt

# Histogram for Gray scale and Color image
 
gray_image = cv2.imread('grayscale.jpeg')
color_image = cv2.imread('color.jpeg')
plt.imshow(gray_image)
plt.show()
plt.imshow(color_image)
plt.show()
hist = cv2.calcHist([gray_image],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('GrayScaleValue')
plt.ylabel('PixelCount')
plt.stem(hist)
plt.show()
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity Value')
plt.ylabel('PixelCount')
plt.stem(hist1)
plt.show()



# Equalized Image
import cv2
Gray_image=cv2.imread('gray.jpeg',0)
equ = cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()






```
## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/22009011/Histogram-of-an-images/assets/118343461/cf331f99-77d8-464c-b26b-6cd679a939e7)


### COLOR IMAGE:
![image](https://github.com/22009011/Histogram-of-an-images/assets/118343461/01876521-e212-4b0e-9831-ca1f7269490a)





### Histogram of Grayscale Image and any channel of Color Image
### GREY SCALE :
![image](https://github.com/22009011/Histogram-of-an-images/assets/118343461/1801eb6a-712e-4da1-b002-5766cd3b96a9)

COLOR SCALE IMAGE:
![image](https://github.com/22009011/Histogram-of-an-images/assets/118343461/629cb394-9dea-4460-b6b5-e8cc0a28d66e)


### Histogram Equalization of Grayscale Image.

### ORIGINAL:
![image](https://github.com/22009011/Histogram-of-an-images/assets/118343461/8656e9db-ed92-4ff4-9e8c-5ddfb4db38fc)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
