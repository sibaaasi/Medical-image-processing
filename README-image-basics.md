# Image Transformations, Edge Detection, and Coin Detection

## Objective

Explore how digital images are represented, transformed, and analyzed, progressing from individual pixel values to detecting circular objects.

## Input Images

The original images are not included.

- **traffic.jpeg:** a color traffic-scene image used for pixel inspection, resizing, grayscale conversion, rotation, and edge detection. The code accesses specific pixel coordinates, so the image must be at least 151 pixels tall and 151 pixels wide.
- **coins.jpeg:** an image containing multiple coins, used for thresholding and circle detection.

## Processing Steps

### Image representation and transformations

The notebook loads a traffic image, inspects its dimensions and pixel values, and demonstrates resizing, grayscale conversion, and a 180-degree rotation.

OpenCV loads color images in BGR order, so the notebook converts them to RGB for display with Matplotlib.

### Edge detection

Sobel derivatives measure intensity changes in the horizontal and vertical directions. Their combined magnitude is thresholded to produce a binary edge image.

A second approach applies Gaussian smoothing followed by a Laplacian operator to highlight intensity changes.

### Coin segmentation and detection

Otsu thresholding separates image regions based on grayscale intensity.

The notebook also displays Canny edges and uses the Hough circle transform to detect coins. Detected circles are drawn over the image, and their diameters are calculated in pixels.

## Outputs

- Transformed images.
- Grayscale and edge images.
- A thresholded coin image.
- Detected circles overlaid on the original image.
- Coin count, individual diameters, and average diameter.

## Notebook

[image_basics_and_coin_detection.ipynb](image_basics_and_coin_detection.ipynb)

## Run

Open the notebook in Google Colab and upload suitable images using the filenames above.

The Hough circle parameters were chosen for the original coin image. Different images may require adjustments to the radius range, minimum distance, and detection thresholds.
