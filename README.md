# Image-Watermarking-through-Entropy-Thresholding

Image Watermarking with Entropy Thresholding

This repository contains Python code for image watermarking using entropy thresholding. The code implements a technique known as Entropy Thresholding (ET) to embed and extract watermarks from digital images.
Introduction

Image watermarking is a method used to embed data into digital images for purposes such as copyright protection and authentication. Entropy Thresholding (ET) is a technique that leverages the entropy of image blocks to determine where to embed the watermark, ensuring both effectiveness and minimal visual impact on the image.
Features

    Embedding Watermarks: The code embeds a binary watermark into an image using ET.
    Extracting Watermarks: It also extracts the watermark from a watermarked image based on predefined threshold and block size.
    Visualization: The code provides visualization of the original image, watermarked image, and the difference between them.

Usage

To use this code:

    Clone the repository to your local machine.
    Ensure you have Python and the required libraries installed (OpenCV, NumPy, Matplotlib, SciPy).
    Run the main.py script with your image file and desired parameters.

Example

python

# Load image
image = cv2.imread('example_image.jpg', 0)

# Generate watermark
watermark = np.random.randint(0, 2, size=100)

# Embed watermark
watermarked_image = embed(image, watermark, threshold=3.5)

# Extract watermark
extracted_watermark = extract(watermarked_image, threshold=3.5, watermark_size=len(watermark))

Acknowledgments

The concept and theory behind this code are adapted from Kaushal M. Solanki's dissertation on multimedia data hiding.
