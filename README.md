
# Image Processing: Edge Detection Using Convolutional Operators

## Objective
To implement and visualize edge detection techniques (Sobel, Scharr, and Canny) on a grayscale image using both custom and library-based approaches.

---

## Workflow Summary

### 1. Library Imports and Image Loading
- Libraries used: `cv2`, `matplotlib`, `numpy`, and `sklearn.metrics`.
- Input image is loaded in both RGB and grayscale formats.

### 2. Grayscale Grid Matrix Generation
- The image is divided into a 162×312 grid.
- Average grayscale values are computed per cell using weighted RGB values:
  - `0.299 R + 0.587 G + 0.114 B`

### 3. Convolution and Gray Scale Conversion
- `convolve()` function performs 2D convolution manually.
- `scaler()` converts the values to 0-255 grayscale

---

## Edge Detection Techniques

### 1. Sobel Edge Detection
- **Filters**: Gx and Gy kernels detect horizontal and vertical edges.
- **Computation**:
  - Euclidean: `sqrt(Gx² + Gy²)`
  - Approximate: `|Gx| + |Gy|`
- **Plots**: I have plotted the results of both the approaches above.

### 2. Scharr Edge Detection
- **Filters**: Modified Gx and Gy according to the Scharr edge detection kernel.
- **Computation**: Same Euclidean formula as Sobel.
- **Visualization**: Side-by-side display of original and processed image.

### 3. Canny Edge Detection
- **Steps**:
  1. Convert to grayscale.
  2. Apply Gaussian Blur to reduce noise.
  3. Use `cv2.Canny()` with thresholds (25, 70) for edge detection with hysteresis.
- **Visualization**: Side-by-side view of the original image and Canny result.

---

## Implemented functions
- `convolve()`: Applies a kernel to a matrix using custom convolution logic.
- `scaler()`: Normalizes matrix values to 0–255.
- `sobel_sqroot()`, `sobel_mod_approx()`, `scharr()`: Compute edge magnitude.
- `cv2.Canny()`: Implements built-in Canny edge detection with automatic thresholding and hysteresis.

---
