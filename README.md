# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.

### Step2:
Load the image file in the program.

### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

### Step4:
Display the modified image output.

### Step5:
End the program.

## Program:
```
Developed By:VAISHNAVI S
Register Number: 212222230165
```
i)Image Translation
```

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread( "car.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis( 'off')
plt.imshow(input_image)
plt.show()
rows,cols,dim =input_image.shape
M =np.float32([[1,0,100],
               [0,1,100],
               [0,0,1]])
translated_image =cv2.warpPerspective(input_image, M, (cols, rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```
ii) Image Scaling
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("timesquare.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M=np.float32([[1.5,0 ,0],
              [0,1.8,0],
              [0,0,1]])
scaled_img=cv2.warpPerspective(in_img, M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
```

iii)Image shearing

```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("sphere.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,0.5,0],
                [0,1 ,0],
                [0,0 ,1]])
M_y=np.float32([[1,  0,0],
                [0.5,1,0],
                [0,  0,1]])
sheared_img_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
sheared_img_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(sheared_img_x)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_y)
plt.show()

```

iv)Image Reflection
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("statue.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,  0,0  ],
                [0,-1,rows],
                [0,0,1  ]])
M_y=np.float32([[-1,0,cols],
                [ 0,1,0  ],
                [ 0,0,1  ]])
reflect_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
reflect_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflect_x)
plt.show()
plt.axis('off')
plt.imshow(reflect_y)
plt.show()  

```



v)Image Rotation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("photograph.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
              [np.sin(angle),np.cos(angle),0],
              [0,0,1]])
rotated_img=cv2.warpPerspective(in_img,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```


vi)Image Cropping

```

import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img = cv2.imread("beach.jpg")
in_img = cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.imshow(in_img)
plt.show()
cropped_img=in_img[50:200 ,50:500]
plt.imshow(cropped_img)
plt.show()

```
## Output:
### i)Image Translation

![311193973-d245bd2d-5114-4e38-8fe6-0c1c3d135942](https://github.com/Vaishnavi-saravanan/IMAGE-TRANSFORMATIONS/assets/118541897/122912f4-87e7-4dd6-aaaf-4f6bcf01fee5)

### ii) Image Scaling
![311194105-4eca9649-368f-46c6-8d43-f1299a6a403f](https://github.com/Vaishnavi-saravanan/IMAGE-TRANSFORMATIONS/assets/118541897/2262e5e0-6fe3-4870-89ea-fd991b62f823)



### iii)Image shearing
![311194462-ad6daa22-a4f5-49b9-9354-638e5fd1e6a0](https://github.com/Vaishnavi-saravanan/IMAGE-TRANSFORMATIONS/assets/118541897/2b2e3576-d715-4eda-86c4-e77bd3676eff)
![311194476-9d92d8de-b3e4-4c4a-97eb-0964e4476004](https://github.com/Vaishnavi-saravanan/IMAGE-TRANSFORMATIONS/assets/118541897/ae285c36-b975-4113-a0bc-636f77eba572)

### iv)Image Reflection

![311194981-8d7de3c2-7521-4421-b4cd-3863136c7abf](https://github.com/Vaishnavi-saravanan/IMAGE-TRANSFORMATIONS/assets/118541897/9fc7186c-dc0e-4a31-a826-d2f55a6b462e)

![311194999-38897a8b-cdc3-4738-a58c-68ae718b8885](https://github.com/Vaishnavi-saravanan/IMAGE-TRANSFORMATIONS/assets/118541897/dcbc99ae-9ad9-4a8e-a7c7-e75460171f6d)


### v)Image Rotation
![311195101-3a6b192f-545e-49de-bada-f8eb6dd20437](https://github.com/Vaishnavi-saravanan/IMAGE-TRANSFORMATIONS/assets/118541897/3df873c8-882a-4fee-bace-b75c28ddc1a6)



### vi)Image Cropping

![311480960-d89dfeaf-b87d-43cf-ac6b-d43b39be1e1e](https://github.com/Vaishnavi-saravanan/IMAGE-TRANSFORMATIONS/assets/118541897/ae5cc66e-6749-4b4c-8919-d3690002c753)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
