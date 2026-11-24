# Detect-the-lines-using-Hough-Transform

##  Aim

To implement a basic lane detection pipeline using OpenCV by completing missing code segments at specified locations.

---

## Learning Objective

* Understand each stage of image processing
* Learn how to build a complete computer vision pipeline
* Practice writing code in guided sections

**Important Instruction:**
👉 Write code **ONLY in places marked as `# Your Code Here`**
👉 Do NOT modify any other part of the code



##  Software Used

* Anaconda – Python 3.7
* Jupyter Notebook / VS Code
* OpenCV (cv2)
* NumPy
* Matplotlib

##  Algorithm & Explanation



###  Step 1: Import Libraries


import cv2
import numpy as np
import matplotlib.pyplot as plt

###  Step 2: Read the Image


# Read the image using OpenCV



###  Step 3: Convert to Grayscale


# Convert to grayscale.



###  Step 4: Display Images


plt.figure(figsize=(10,5))


###  Step 5: Thresholding

# Apply thresholding



###  Step 6: Region of Interest (ROI)


# ROI masking already provided
# (Do not modify)

### Step 7: Edge Detection (Canny)

# Perform Edge Detection



###  Step 8: Gaussian Blur


# Apply Gaussian Blur

###
# Your Code Here
###




###  Step 9: Hough Transform


# Detect lines using Hough Transform



### Step 10: Lane Detection Logic



### Program
```
# Step 2: Load the image using imread() from cv2 module
image = cv2.imread('img.jpg')  # Replace 'image.jpg' with your image path
# Step 3: Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Input image and grayscale image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert image to RGB for displaying
plt.title("Input Image")
plt.axis('off')
(np.float64(-0.5), np.float64(1079.5), np.float64(1281.5), np.float64(-0.5))

plt.imshow(gray_image, cmap='gray')
plt.title("Grayscale Image")
plt.axis('off')
(np.float64(-0.5), np.float64(1079.5), np.float64(1281.5), np.float64(-0.5))

# Step 4: Using Canny operator from cv2, detect the edges of the image
edges = cv2.Canny(gray_image, 50, 150)  # Canny edge detection with threshold values 50 and 150
# Canny Edge Detector output
plt.imshow(edges, cmap='gray')
plt.title("Canny Edge Detector")
plt.axis('off')
(np.float64(-0.5), np.float64(1079.5), np.float64(1281.5), np.float64(-0.5))

# Step 5: Using the HoughLinesP(), detect line coordinates for every point in the image
# The parameters of HoughLinesP are: image, resolution, threshold, minLineLength, maxLineGap
lines = cv2.HoughLinesP(edges, 1, np.pi / 180, 100, minLineLength=50, maxLineGap=10)
# Step 6: Using a for loop, draw the lines on the original image using the detected coordinates
# The lines variable contains the endpoints of the detected lines
for line in lines:
    x1, y1, x2, y2 = line # Unpacking the line coordinates
    cv2.line(image, (x1, y1), (x2, y2), (0, 255, 0), 2)  # Draw green lines with thickness of 2
# Display the result of Hough Transform (Image with lines)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Image with lines drawn
plt.title("Result of Hough Transform")
plt.axis('off')
(np.float64(-0.5), np.float64(1079.5), np.float64(1281.5), np.float64(-0.5))

 
 
```
##  Expected Output


* <img width="482" height="522" alt="image" src="https://github.com/user-attachments/assets/3669c31d-fe91-4d17-81d0-d9d8cabad8e0" />


* <img width="452" height="518" alt="image" src="https://github.com/user-attachments/assets/f972a709-8f91-4bd9-ae89-305c2dab77f9" />


* <img width="447" height="516" alt="image" src="https://github.com/user-attachments/assets/97c1cdaf-6cad-49a9-9ac6-8c55b329987c" />


* <img width="463" height="523" alt="image" src="https://github.com/user-attachments/assets/06039db3-7ac7-4fab-8370-7b8fc582bffe" />



---

##  Instructions

* Fill ONLY in `# Your Code Here` sections
* Do NOT change existing code
* Run step-by-step
* Verify outputs

---

## Result

Thus, the lane detection pipeline is successfully implemented by completing the missing code sections. The system detects and highlights lane lines effectively.

---

##  Developed By

* **Name:** _____AATHI S______________________
* **Register No:** ___212223220001___________________
