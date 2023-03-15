# READ AND WRITE AN IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.
i) Read, display, and write an image.
ii) Access the rows and columns in an image.
iii) Cut and paste a small portion of the image.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
## Program:
### Developed By:YASHASWI MITTA
### Register Number: 212221230062
i) #To Read,display the image
```
import cv2
from google.colab.patches import cv2_imshow
a = cv2.imread('/content/bird.jpg',1)
cv2_imshow(a)
cv2.waitKey(0)   

```
ii) #To write the image
```
colorImage = cv2.imread('/content/bird.jpg',1)
cv2.imwrite('written.jpg',colorImage)
writtenImage = cv2.imread('written.jpg',1)
cv2_imshow(writtenImage)
cv2.waitKey(0)


```
iii) #Find the shape of the Image
```python3
colorImage = cv2.imread('/content/bird.jpg',1)
print(colorImage.shape)



```
iv) #To access rows and columns

```python3
import random
colorImage = cv2.imread('/content/bird.jpg',1)
for i in range(100):
    for j in range(colorImage.shape[1]):
        colorImage[i][j]=[random.randint(0,255),random.randint(0,255),random.randint(0,255)]
cv2_imshow(colorImage)
cv2.waitKey(0)


```
v) #To cut and paste portion of image
```python3
color_img = cv2.imread('/content/bird.jpg',1)
tag = color_img[200:400,300:500]
color_img[200:400,100:300] = tag
cv2_imshow(color_img)
cv2.waitKey(0)


```

## Output:

### i) Read and display the image
![1](https://user-images.githubusercontent.com/94619247/225367080-6151e33c-105d-413a-b73e-cbf6ef3ffd53.png)



### ii)Write the image
![2](https://user-images.githubusercontent.com/94619247/225366787-4147b006-e4ef-4c0b-89c9-7f69af5f928e.png)



### iii)Shape of the Image
![3](https://user-images.githubusercontent.com/94619247/225366873-9b4e9f92-4362-4648-adbe-73ce939ec9a0.jpg)



### iv)Access rows and columns
![4](https://user-images.githubusercontent.com/94619247/225366909-ea4f5251-4b7b-4804-b6b8-08d122ba1fec.png)




### v)Cut and paste portion of image
![5](https://user-images.githubusercontent.com/94619247/225367017-c5d1910f-9aec-4be9-9655-02266d0d48f1.png)




## Result:
Thus the images are read, displayed, and written successfully using the python program.


