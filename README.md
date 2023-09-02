# HISTOGRAM
# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

Step1: Import the necessary libraries and read two images, Color image and Gray Scale image.

Step2: Calculate the Histogram of Gray scale image and each channel of the color image.

Step3: Display the histograms with their respective images.

Step4: Equalize the grayscale image.

Step5: Display the grayscale image.

## Program:
```python
# Developed By : D.vishnu vardhan reddy
# Register Number: 212221230023
import cv2
import matplotlib.pyplot as plt

### Write your code to find the histogram of gray scale image and color image channels.

gray_image=cv2.imread('cat.jpg')
hist=cv2.calcHist([gray_image],[0],None,[256],[0,256])
plt.imshow(gray_image)
plt.show()
plt.figure()
plt.title("histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()





# Display the histogram of gray scale image and any one channel histogram from color image
color_image=cv2.imread('car.jpg')
hist1=cv2.calcHist([color_image],[1],None,[256],[0,256])
plt.imshow(color_image)
plt.show()
plt.figure()
plt.title("histogram of color image :Green channel")
plt.xlabel('intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()




# Write the code to perform histogram equalization of the image. 
gray_image = cv2.imread('cycle.jpg',0)
equ=cv2.equalizeHist(gray_image)
cv2.imshow('Gray image',gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()






```
## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/vishnudorigundla/HISTOGRAM/assets/94175324/a687d99a-47cc-486a-8925-2af63dd66654)

![image](https://github.com/vishnudorigundla/HISTOGRAM/assets/94175324/e60ce448-8947-4fbe-980e-85536186e987)

### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/vishnudorigundla/HISTOGRAM/assets/94175324/144a2f5c-0fb6-4037-9f40-4d55129457f6)
![image](https://github.com/vishnudorigundla/HISTOGRAM/assets/94175324/6c917aa3-2f43-4ba7-a9ae-7ec486b0145a)


### Histogram Equalization of Grayscale Image
![image](https://github.com/vishnudorigundla/HISTOGRAM/assets/94175324/d7f8a6eb-a0c1-4e40-afab-9e1c33b3ca73)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
