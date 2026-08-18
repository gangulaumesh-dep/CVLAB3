# Computer Vision Lab 3 – Average Filtering

## 📌 Overview

This project demonstrates **Average Filtering in Computer Vision** using Python. The experiment applies different average filter kernel sizes to a grayscale image and compares the resulting blurred images.

The implementation uses **OpenCV, NumPy, and Matplotlib**.

## 🎯 Objective

To implement and visualize average filtering using different kernel sizes:

* 3 × 3 Average Filter
* 5 × 5 Average Filter
* 7 × 7 Average Filter

The experiment helps understand how increasing the kernel size affects image smoothing and blurring.

## 🛠️ Technologies Used

* Python 3
* OpenCV (`cv2`)
* NumPy
* Matplotlib
* Google Colab / Jupyter Notebook

## 📂 Project Structure

```text
Computer-Vision-Lab-3/
│
├── CV_LAB3.ipynb
├── cv3.jpg
├── average_filter_output.png
└── README.md
```

## 🔬 Experiment

The input image is converted/read as a **grayscale image**. Average filter kernels are created using NumPy.

### 3 × 3 Kernel

```python
kernel_3x3 = np.ones((3, 3), np.float32) / 9
```

### 5 × 5 Kernel

```python
kernel_5x5 = np.ones((5, 5), np.float32) / 25
```

### 7 × 7 Kernel

```python
kernel_7x7 = np.ones((7, 7), np.float32) / 49
```

The filters are applied using OpenCV's `filter2D()` function.

```python
blur3 = cv2.filter2D(img, -1, kernel_3x3)
blur5 = cv2.filter2D(img, -1, kernel_5x5)
blur7 = cv2.filter2D(img, -1, kernel_7x7)
```

## 📊 Output

The program displays four images:

1. Original Grayscale Image
2. Average Filter (3 × 3)
3. Average Filter (5 × 5)
4. Average Filter (7 × 7)

The notebook also saves the resulting comparison as:

```text
average_filter_output.png
```

## 📚 Libraries

### OpenCV

Used for reading the image and applying the filtering operation.

### NumPy

Used to create the average filter kernels.

### Matplotlib

Used to display and compare the original and filtered images.

## ▶️ How to Run

### Option 1: Google Colab

1. Open the `CV_LAB3.ipynb` notebook in Google Colab.
2. Upload the `cv3.jpg` image.
3. Update the image path if required.
4. Run all cells.
5. View the filtered images.

### Option 2: Jupyter Notebook

Install the required libraries:

```bash
pip install opencv-python numpy matplotlib
```

Then open:

```text
CV_LAB3.ipynb
```

and run the cells.

## 💡 Result

The experiment demonstrates that average filtering smooths the image by averaging neighboring pixel values. As the kernel size increases from **3 × 3 to 7 × 7**, the smoothing and blurring effect becomes stronger.

## 👨‍💻 Author

**Computer Vision Laboratory**

---

⭐ If you find this project useful, consider giving the repository a star!
