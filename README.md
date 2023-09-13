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
````
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
```



```
## Output:
### i)Image Translation

![WhatsApp Image 2023-09-13 at 15 49 29](https://github.com/Jeevithaelumalai/IMAGETRANSFORMATION/assets/118708245/7a520242-95e3-4dbf-bbf7-9702533ccd00)

### ii) Image Scaling

![WhatsApp Image 2023-09-13 at 15 49 45](https://github.com/Jeevithaelumalai/IMAGETRANSFORMATION/assets/118708245/e19e2bb6-c894-4e9b-974b-0c79c8f1882c)


### iii)Image shearing
![WhatsApp Image 2023-09-13 at 15 50 05](https://github.com/Jeevithaelumalai/IMAGETRANSFORMATION/assets/118708245/b6ca83b5-62b9-4fba-bbfd-3c0e5541b944)

![WhatsApp Image 2023-09-13 at 15 50 30](https://github.com/Jeevithaelumalai/IMAGETRANSFORMATION/assets/118708245/08c759f6-68dc-429e-b8fe-fafa0925c102)

![WhatsApp Image 2023-09-13 at 15 51 26](https://github.com/Jeevithaelumalai/IMAGETRANSFORMATION/assets/118708245/47c98d30-3321-4e79-891e-848e863c5d06)

### iv)Image Reflection

![WhatsApp Image 2023-09-13 at 15 51 41](https://github.com/Jeevithaelumalai/IMAGETRANSFORMATION/assets/118708245/28c36d82-5915-4918-b9a7-f03d6349ea7a)

![WhatsApp Image 2023-09-13 at 15 51 57](https://github.com/Jeevithaelumalai/IMAGETRANSFORMATION/assets/118708245/d742c529-ac23-41fa-8baa-58ad9aea2d9b)

![WhatsApp Image 2023-09-13 at 15 52 12](https://github.com/Jeevithaelumalai/IMAGETRANSFORMATION/assets/118708245/f1ae4765-56f0-4d83-948c-89c1eba4a7e8)


### v)Image Rotation
![WhatsApp Image 2023-09-13 at 15 52 28](https://github.com/Jeevithaelumalai/IMAGETRANSFORMATION/assets/118708245/b0cddfe0-a17a-4b86-9d40-97e856548169)


### vi)Image Cropping

![WhatsApp Image 2023-09-13 at 15 52 48](https://github.com/Jeevithaelumalai/IMAGETRANSFORMATION/assets/118708245/51e1116a-38c7-46cf-96ac-b9dd8583df3c)




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
