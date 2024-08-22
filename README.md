# Workshop--1-Working-on-an-Image


1.Load two images of the same size.

2. Divide each image into four equal regions (quadrants) based on specific row and column coordinates.
3. 
4. Save the eight individual regions, labeling them as R1, R2, R3, R4 for the first image and R5, R6, R7, R8 for the second image.
5. 
6. Swap the regions as follows:
        R1 with R8
        R2 with R7
   
8. Resize the final images to dimensions specified by the last four digits of your registration number, ensuring the number is even.

# Program:
```
import cv2

# Load the images

image1 = cv2.imread('08.JPG')

image2 = cv2.imread('08a.JPG')

image1.shape

image2.shape

image1_resized = cv2.resize(image1, (400,400))

image2_resized = cv2.resize(image1, (400,400))

image1_resized.shape

image2_resized.shape

## Split the image into 4 regions using row and column coordinates

R1 = image1_resized [0:200, 0:200] #Top-Left region

R2 = image1_resized [0:200, 200:400] # Top-right region

R3 image1_resized [200:400, 0:200] # Bottom-left region

R4 = image1_resized [200:400, 200:400] # Bottom-right region


R5 = image2_resized [0:200, 0:200] #Top-Left region

R6= image2_resized [0:200, 200:400] # Top-right region

R7 = image2_resized [200:400, 0:200] # Bottom-left region

R8 = image2_resized 200:400, 200:400] # Bottom-right region


image1_resized [0:200, 0:200] = R8

image2_resized [200:400, 200:400] =R3


#Display the resized images

cv2.imshow('Resized Image 1', image1_resized)

cv2.imshow('Resized Image 2', image2_resized)

cv2.waitKey(0)

cv2.destroyAllWindows()
```

# Output:

![Resized Image 1](https://github.com/user-attachments/assets/877082b8-ff37-4a50-a7bc-5f2a6bb0fa5f)



![Resized Image 2](https://github.com/user-attachments/assets/cee42089-d9ef-4a13-965a-a496b3cf7b36)




