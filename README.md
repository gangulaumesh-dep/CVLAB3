# Computer Vision Laboratory – Average Filtering

## Introduction

This repository contains the implementation of an image smoothing experiment using **Average Filtering** in Computer Vision.

The experiment applies average filters with different kernel sizes to a grayscale image and compares their effects. The implementation is developed using Python with OpenCV, NumPy, and Matplotlib.

## Objective

The objective of this experiment is to understand the working of an average filter and observe how different kernel sizes affect image smoothing.

The following filters are implemented:

* 3 × 3 Average Filter
* 5 × 5 Average Filter
* 7 × 7 Average Filter

## Technologies Used

* Python 3
* OpenCV
* NumPy
* Matplotlib
* Google Colab / Jupyter Notebook

## Repository Contents

```text
Computer-Vision-Lab/
│
├── CV_LAB3.ipynb
├── cv3.jpg
├── average_filter_output.png
└── README.md
```

### File Description

| File                        | Description                                                          |
| --------------------------- | -------------------------------------------------------------------- |
| `CV_LAB3.ipynb`             | Jupyter/Google Colab notebook containing the complete implementation |
| `cv3.jpg`                   | Input image used for the experiment                                  |
| `average_filter_output.png` | Output containing the original and filtered images                   |
| `README.md`                 | Documentation for the project                                        |

## Methodology

The input image is loaded as a grayscale image. Three average filter kernels are created using NumPy.

### 3 × 3 Average Filter

```python
kernel_3x3 = np.ones((3, 3), np.float32) / 9
```

### 5 × 5 Average Filter

```python
kernel_5x5 = np.ones((5, 5), np.float32) / 25
```

### 7 × 7 Average Filter

```python
kernel_7x7 = np.ones((7, 7), np.float32) / 49
```

The filters are applied to the image using OpenCV's `filter2D()` function:

```python
blur3 = cv2.filter2D(img, -1, kernel_3x3)
blur5 = cv2.filter2D(img, -1, kernel_5x5)
blur7 = cv2.filter2D(img, -1, kernel_7x7)
```

The implementation and filter sizes are based on the uploaded laboratory notebook.

## Output

The program displays four images for comparison:

1. Original Grayscale Image
2. Image after applying the 3 × 3 Average Filter
3. Image after applying the 5 × 5 Average Filter
4. Image after applying the 7 × 7 Average Filter

The notebook also saves the output as:

```text
average_filter_output.png
```

The output visualization and saving operation are implemented in the notebook.

## Observations

The average filter replaces each pixel with the average value of its neighboring pixels.

As the kernel size increases:

* The amount of smoothing increases.
* Fine image details become less visible.
* The image becomes progressively more blurred.
* Larger kernels produce stronger smoothing effects.

## How to Run

### Using Google Colab

1. Upload `CV_LAB3.ipynb` to Google Colab.
2. Upload the input image `cv3.jpg`.
3. Make sure the image path in the notebook points to the correct location.
4. Run all cells.
5. View the generated filtered images.

### Using Jupyter Notebook

Install the required libraries:

```bash
pip install opencv-python numpy matplotlib
```

Open the notebook:

```text
CV_LAB3.ipynb
```

Run all cells to perform the experiment.

## Requirements

The experiment requires the following Python libraries:

```text
opencv-python
numpy
matplotlib
```

## Result

The experiment successfully demonstrates average filtering using 3 × 3, 5 × 5, and 7 × 7 kernels. The comparison shows the effect of increasing kernel size on image smoothing and blurring.

## Conclusion

Average filtering is a simple spatial filtering technique used to reduce image variations and smooth images. By comparing different kernel sizes, the experiment demonstrates that larger kernels produce a stronger smoothing effect.

## Author

Computer Vision Laboratory Project
