# Object Counting and Brain-Image Segmentation

This project contains two notebooks exploring how filtering, segmentation, and connected-component analysis can identify regions in images.

## Part 1: Object Counting

### Objective

Separate and count objects in a noisy grayscale image.

### Method

1. Apply Otsu thresholding to obtain a binary image.
2. Apply a median filter and repeat thresholding to reduce noise.
3. Extract object boundaries by subtracting an eroded image from the binary image.
4. Use flood filling to fill enclosed regions.
5. Label the resulting objects using 8-connected component analysis.

The notebook displays intermediate processing stages, reports the object count, and visualizes component labels using different gray levels.

**Notebook:** [object_counting.ipynb](object_counting.ipynb)

**Input image:**

**pic1dirty.jpg:** a noisy grayscale image containing objects to separate and count. It is used to demonstrate median filtering, thresholding, boundary extraction, region filling, and connected-component labeling.
The original image is not included. Upload a suitable replacement using the same filename.

## Part 2: Brain-Image Segmentation

### Objective

Explore intensity-based clustering and morphological processing on a grayscale brain image.

### Method

1. Treat each pixel intensity as a sample for K-means clustering.
2. Compare segmentations using 3, 4, and 5 clusters.
3. Apply connected-component labeling within the four-cluster segmentation.
4. Select the cluster with the highest mean intensity.
5. Apply morphological opening and closing to clean the selected mask.
6. Select a candidate region using component area and proximity to a predefined location.

The final region selection uses assumptions specific to this example image, rather than a trained tumor-detection model.

**Notebook:** [brain_image_segmentation.ipynb](brain_image_segmentation.ipynb)

**Input image:** 

**brain.jpg:** a grayscale brain image used to explore intensity clustering, connected components, and morphological processing.
The original image is not included. Upload a suitable replacement using the same filename.
The final region-selection step assumes a bright region near a predefined location and within a specified area range. These assumptions may need adjustment for another image.

## Run

Open either notebook in Google Colab. Run its first cell and upload the corresponding image when prompted, then run the remaining cells in order.
Dependencies: OpenCV, NumPy, and Matplotlib.
