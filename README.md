# EX.NO-9-Record-IMPLEMENTATION-OF-EROSION-AND-DILATION

Exp:9-RECORD IMPLEMENTATION OF EROSION AND DILATION

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

Image Erosion Image Dilation

Software Used

Anaconda – Python 3.7 Jupyter Notebook / VS Code OpenCV (cv2) NumPy Matplotlib

Algorithm

Step 1: Import the required libraries: OpenCV, NumPy, and Matplotlib.

Step 2: Create a blank image using NumPy.

Step 3: Insert text onto the image using OpenCV's text drawing function.

Step 4: Display the original image.

Step 5: Create a structuring element (kernel) of suitable size.

Step 6: Image Erosion Apply the erosion operation using the created kernel. Remove pixels from the boundaries of foreground objects. Display the eroded image. Step 7: Image Dilation Apply the dilation operation using the same kernel. Add pixels to the boundaries of foreground objects. Display the dilated image. Step 8: Compare the original, eroded, and dilated images.

Developed By

Name: DEEPIKA V

Register No: 212224240030

Program
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)

# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'DEEPIKA', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Input Image with Text")
plt.axis('off')

# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)

# Apply erosion (shrinking effect)
eroded_image = cv2.erode(image, kernel, iterations=1)

# Display the eroded image
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))
plt.title("Eroded Image")
plt.axis('off')

# Apply dilation (expanding effect)
dilated_image = cv2.dilate(image, kernel, iterations=1)

# Display the dilated image
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))
plt.title("Dilated Image")
plt.axis('off')
```
## OUTPUT:

Original Image

<img width="381" height="398" alt="image" src="https://github.com/user-attachments/assets/97e55432-9e5d-4be8-80b4-81932522b346" />


A text image containing characters is displayed.

The image serves as the input for morphological processing.

Erosion

<img width="381" height="405" alt="image" src="https://github.com/user-attachments/assets/31bb714b-6660-4522-a9c6-ae3251246f15" />

Original image is displayed.

Eroded image is displayed.

The thickness of the characters is reduced.

Object boundaries shrink inward.

Dilation

<img width="374" height="398" alt="image" src="https://github.com/user-attachments/assets/b87f6586-c95d-492c-8520-a5b961aed92e" />

Original image is displayed.

Dilated image is displayed.

The thickness of the characters increases.

Object boundaries expand outward. Result Thus, the morphological operations Erosion and Dilation are successfully implemented using OpenCV.
A text image containing characters is displayed.

