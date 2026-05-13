# Histogram-processing

## Aim

To write a Python program using OpenCV to perform histogram equalization on both grayscale and color images to enhance image contrast and brightness.

The program performs the following operations:

- Read and display a grayscale image  
- Plot histogram of the grayscale image  
- Apply histogram equalization on grayscale image  
- Read and display a color image  
- Plot histogram of B, G, R channels  
- Convert image to HSV color space  
- Apply histogram equalization on the Value (V) channel  
- Convert the enhanced image back to BGR format  
- Display original and enhanced images with histograms  


## Software Used

- Anaconda – Python 3.7  
- Jupyter Notebook / VS Code  
- OpenCV (`cv2`)  
- NumPy  
- Matplotlib  


## Algorithm

### Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:
Read the image `parrot.jpg` in grayscale format.

### Step 3:
Display the grayscale image and plot its histogram.

### Step 4:
Apply histogram equalization using `cv2.equalizeHist()` to enhance contrast.

### Step 5:
Display original grayscale image, its histogram, enhanced image, and its histogram using a 2 × 2 grid.

### Step 6:
Read the same image in color format.

### Step 7:
Split the image into B, G, R channels and plot their histograms.

### Step 8:
Convert the image from BGR to HSV color space.

### Step 9:
Apply histogram equalization on the V (Value) channel.

### Step 10:
Merge the channels and convert the image back to BGR format.

### Step 11:
Display original color image, histogram, enhanced image, and enhanced histogram using a 2 × 2 grid.



## Program

### Developed By:
**Name:VEDHANTH H**  
### Register No: 212224240181


#### Input Grayscale Image and Color Image
```
import cv2
from matplotlib import pyplot as plt
# Load the color image
image = cv2.imread('dipt.jpeg')
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
##  Output
<img width="713" height="454" alt="image" src="https://github.com/user-attachments/assets/cec74aed-bfec-481e-a9db-e4b5002076db" />
#### Histogram of Grayscale Image
```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
## Output 

<img width="752" height="594" alt="image" src="https://github.com/user-attachments/assets/b3a410c0-af31-41ef-afb1-fc9f510b3af2" />

#### Histogram Equalization of Grayscale Image
```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='grey')
plt.title('Equalized Image')
plt.axis('off')
```
### Output:
<img width="849" height="451" alt="image" src="https://github.com/user-attachments/assets/9b5de5b0-6d53-4dc0-b4fa-17ef6bdf4eea" />



### Equalized Histogram 
```
hist_original = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```

## Output:

<img width="848" height="573" alt="image" src="https://github.com/user-attachments/assets/c209ec31-e55b-4fcd-98c5-d2826f2efdfc" />


### Grayscale Histogram Equalization

- Original grayscale image is displayed  
- Histogram of original grayscale image is plotted  
- Enhanced image after histogram equalization is displayed  
- Histogram of enhanced grayscale image shows improved contrast  

### Color Image Histogram Equalization

- Original color image is displayed  
- Histogram of B, G, R channels is plotted  
- Enhanced image after HSV-based equalization is displayed  
- Histogram of enhanced image shows better intensity distribution  



## Result

Thus, histogram equalization is successfully performed on both grayscale and color images using OpenCV. The contrast and brightness of the images are significantly improved, enhancing visual quality and feature visibility.
