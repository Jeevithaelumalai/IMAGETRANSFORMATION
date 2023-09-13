# IMAGETRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import the necessary libraries and read the original image and save it as a image variable.
### Step2:
Translate the image
### Step3:
Scale the image

### Step4:
Shear the image.

### Step5:
Find reflection of image.
### step6:
Rotate the image.

### Step7:
Crop the image.

### Step8:
Display all the Transformed images.

## Program:
```python
Developed By: JEEVITHA E
Register Number:212222230054
```
i)Image Translation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M = np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
translated_image = cv2.warpPerspective(lion_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```

ii) Image Scaling
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M = np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
scaled_img = cv2.warpPerspective(lion_image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
```



iii)Image shearing
```

import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(lion_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(lion_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()
```


iv)Image Reflection
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
dog_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(lion_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(lion_image,M_Y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()
```



v)Image Rotation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
angle = np.radians(30)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(lion_image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```




vi)Image Cropping

import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
cropped_img=lion_image[11:500,27:630]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()

## Output:
### i)Image Translation

![WhatsApp Image 2023-09-13 at 15 49 29](https://github.com/Jeevithaelumalai/IMAGETRANSFORMATION/assets/118708245/27601201-ae97-42c7-a29a-80079e0e82f2)



### ii) Image Scaling

![WhatsApp Image 2023-09-13 at 15 49 45](https://github.com/Jeevithaelumalai/IMAGETRANSFORMATION/assets/118708245/e49054ee-ca1f-48f8-b825-7060787ea95a)



### iii)Image shearing
![WhatsApp Image 2023-09-13 at 15 50 05](https://github.com/Jeevithaelumalai/IMAGETRANSFORMATION/assets/118708245/5e52a19b-8046-4cf9-9555-75b338e79581)


![WhatsApp Image 2023-09-13 at 15 50 30](https://github.com/Jeevithaelumalai/IMAGETRANSFORMATION/assets/118708245/90c3a8d0-83a0-4277-9ad5-c34541a7c72f)


![WhatsApp Image 2023-09-13 at 15 51 26](https://github.com/Jeevithaelumalai/IMAGETRANSFORMATION/assets/118708245/caf37340-07a7-44e1-a9c0-aeebfb49c12d)



### iv)Image Reflection


![WhatsApp Image 2023-09-13 at 15 51 41](https://github.com/Jeevithaelumalai/IMAGETRANSFORMATION/assets/118708245/8c74187f-e740-4ffd-9823-9f689abb52b5)


![WhatsApp Image 2023-09-13 at 15 51 57](https://github.com/Jeevithaelumalai/IMAGETRANSFORMATION/assets/118708245/88fb9fc5-67ad-4795-8009-3c2d4cf6a0a1)

![WhatsApp Image 2023-09-13 at 15 52 12](https://github.com/Jeevithaelumalai/IMAGETRANSFORMATION/assets/118708245/6497e1cd-598d-4182-9e2e-eb6186f036f2)


### v)Image Rotation

![WhatsApp Image 2023-09-13 at 15 52 48](https://github.com/Jeevithaelumalai/IMAGETRANSFORMATION/assets/118708245/4507348a-2aec-47a7-831f-f777f4eae2f0)



### vi)Image Cropping


![WhatsApp Image 2023-09-13 at 15 52 28](https://github.com/Jeevithaelumalai/IMAGETRANSFORMATION/assets/118708245/970c4132-3623-4be9-96c1-b281782bd375)




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
