# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Create a blank image using NumPy.

### Step 3:

Insert text onto the image using OpenCV's text drawing function.

### Step 4:

Display the original image.

### Step 5:

Create a structuring element (kernel) of suitable size.

### Step 6: Image Erosion

- Apply the erosion operation using the created kernel.
- Remove pixels from the boundaries of foreground objects.
- Display the eroded image.

### Step 7: Image Dilation

- Apply the dilation operation using the same kernel.
- Add pixels to the boundaries of foreground objects.
- Display the dilated image.

### Step 8:

Compare the original, eroded, and dilated images.

## Output:

### Display the input Image
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("nature.jpeg")
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")
plt.show()
```

<img width="826" height="817" alt="download" src="https://github.com/user-attachments/assets/88a9f864-424e-46b1-9d9c-85c7019f641f" />

### Display the Eroded Image
```
kernel = np.ones((5,5), dtype=np.uint8)
erosion = cv2.erode(img, kernel, iterations=1)
display_img(erosion)
```
<img width="826" height="817" alt="download" src="https://github.com/user-attachments/assets/78495056-2b53-452e-b84d-f804848c5614" />


### Display the Dilated Image
```
dilation = cv2.dilate(img, kernel, iterations=1)
display_img(dilation)
```

<img width="826" height="817" alt="download" src="https://github.com/user-attachments/assets/457b5be9-ed99-4c45-bf96-3b0ba70e9c0e" />

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
