# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

### Step1:
Import all the necessary modules  

### Step2:
Choose an image and save it as filename.jpg

### Step3:
Use imread to read the image

### Step4:
Use cv2.warpPerspective(image,M,(cols,rows)) to translation the image

### Step5:
Use cv2.warpPerspective(image,M,(cols2,rows2)) to scale the image

### Step6:
Use cv2.warpPerspective(image,M,(int(cols1.5),int(rows1.5))) for x and y axis to shear the image

### Step7:
Use cv2.warpPerspective(image,M,(int(cols),int(rows))) for x and y axis to reflect the image

### Step8:
Use cv2.warpPerspective(image,M,(int(cols),int(rows))) to rotate the image

### Step9:
Crop the image to remove unwanted areas from an image

### Step10:
Use cv2.imshow to show the image

### Step11:
End the program

## Program:
```python

Developed By: Karsavarthan R R
Register Number: 212223230100

i)Image Translation

import cv2
import matplotlib.pyplot as plt

image = cv2.imread('image.jpg')

plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  
plt.title("Original Image")
plt.axis('off')   

tx, ty = 100, 120
M_translation = np.float32([[1, 0, tx], [0, 1, ty]]) 
translated_image = cv2.warpAffine(image, M_translation, (image.shape[1], image.shape[0]))

plt.imshow(cv2.cvtColor(translated_image, cv2.COLOR_BGR2RGB))  
plt.title("Translated Image")  
plt.axis('off')

ii) Image Scaling

fx, fy = 5.0, 15.0 
scaled_image = cv2.resize(image, None, fx=fx, fy=fy, interpolation=cv2.INTER_LINEAR)

plt.imshow(cv2.cvtColor(scaled_image, cv2.COLOR_BGR2RGB))  
plt.title("Scaled Image") 
plt.axis('off')

iii)Image shearing

shear_matrix = np.float32([[1, 0.5, 0], [0.5, 1, 0]]) 
sheared_image = cv2.warpAffine(image, shear_matrix, (image.shape[1], image.shape[0]))

plt.imshow(cv2.cvtColor(sheared_image, cv2.COLOR_BGR2RGB)) 
plt.title("Sheared Image") 
plt.axis('off')

iv)Image Reflection

reflected_image = cv2.flip(image, 2)

plt.imshow(cv2.cvtColor(reflected_image, cv2.COLOR_BGR2RGB))
plt.title("Reflected Image")
plt.axis('off')

v)Image Rotation

(h, w) = image.shape[:2]
M = cv2.getRotationMatrix2D((w // 2, h // 2), 45, 1)
rotated = cv2.warpAffine(image, M, (w, h))

plt.imshow(cv2.cvtColor(rotated_image, cv2.COLOR_BGR2RGB)) 
plt.title("Rotated Image") 
plt.axis('off')

vi)Image Cropping

x, y, w, h = 100, 100, 200, 150 
cropped_image = image[y:y+h, x:x+w]

plt.imshow(cv2.cvtColor(cropped_image, cv2.COLOR_BGR2RGB)) 
plt.title("Cropped Image")
plt.axis('off')

```
## Output:

### Orginal image

![Screenshot 2025-04-30 103826](https://github.com/user-attachments/assets/f76abd27-2fbf-49a1-a6e2-733b03564c4e)



### i)Image Translation

![Screenshot 2025-04-30 103935](https://github.com/user-attachments/assets/7ec6de36-e398-4fcc-8360-56e7678cb241)



### ii) Image Scaling

![Screenshot 2025-04-30 103942](https://github.com/user-attachments/assets/f120a6df-bb86-457a-b317-b7ad8c876347)



### iii)Image shearing

![Screenshot 2025-04-30 103948](https://github.com/user-attachments/assets/9226cc16-058a-44e4-822a-643ddda348ee)



### iv)Image Reflection


![Screenshot 2025-04-30 103955](https://github.com/user-attachments/assets/47aaee2e-0a1b-48db-bfa2-5416701d6afb)




### v)Image Rotation


![Screenshot 2025-04-30 103959](https://github.com/user-attachments/assets/c8cf7949-0a3f-4cfd-8b5a-dc8cfd040ef4)




### vi)Image Cropping


![Screenshot 2025-04-30 104005](https://github.com/user-attachments/assets/1590f429-6280-4d31-b610-a3b2fc0176fb)




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
