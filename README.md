# COMPUER-VISION-ITA0541-

# Step 1: Import required libraries
import cv2
import matplotlib.pyplot as plt

# Step 2: Upload image from your system
from google.colab import files
uploaded = files.upload()

# Step 3: Read the uploaded image
image_path = list(uploaded.keys())[0]
img = cv2.imread(image_path)

# Step 4: Convert BGR (OpenCV default) to RGB for correct display
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

# Step 5: Convert image to Grayscale
gray_img = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

# Step 6: Display Original and Grayscale images
plt.figure(figsize=(10,5))

# Original Image
plt.subplot(1,2,1)
plt.imshow(img_rgb)
plt.title("Original Image")
plt.axis('off')

# Grayscale Image
plt.subplot(1,2,2)
plt.imshow(gray_img, cmap='gray')
plt.title("Grayscale Image")
plt.axis('off')

plt.show()
