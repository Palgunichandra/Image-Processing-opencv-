# Image Processing with OpenCV

This project demonstrates various image processing techniques using OpenCV.

## Requirements

- Python 3.x
- OpenCV
- NumPy
- Matplotlib

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/image-processing-opencv.git
   cd image-processing-opencv
pip install opencv-python numpy matplotlib
import cv2
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('path/to/your/image.jpg')

# Display the image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.axis('off')
plt.show()

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Display the grayscale image
plt.imshow(gray_image, cmap='gray')
plt.axis('off')
plt.show()
blurred_image = cv2.GaussianBlur(gray_image, (5, 5), 0)

# Display the blurred image
plt.imshow(blurred_image, cmap='gray')
plt.axis('off')
plt.show()
edges = cv2.Canny(blurred_image, 100, 200)

# Display the edges
plt.imshow(edges, cmap='gray')
plt.axis('off')
plt.show()

