# Enhancing Facial Recognition Accuracy Through Image Processing Techniques

## 📌 Project Overview

Facial recognition systems can be affected by low-quality images, noise, varying illumination, and other image-related challenges.

This project investigates how image processing and enhancement techniques can improve the performance of a Convolutional Neural Network (CNN) for facial recognition.

The project applies a sequence of image enhancement techniques to grayscale facial images and compares recognition performance before and after enhancement.

---

## 🎯 Objectives

* Improve the quality and clarity of low-resolution facial images.
* Reduce image noise and enhance important facial details.
* Apply different image processing techniques before model training.
* Train a CNN-based facial recognition model.
* Compare recognition performance before and after image enhancement.

---

## 🗂️ Dataset

The project uses a facial image dataset containing **1,005 grayscale images of 10 individuals**.

The images contain variations in:

* Lighting conditions
* Facial poses and angles
* Image quality
* Resolution

The dataset is organized by individual/class before being processed.

> **Note:** The dataset is not included in this repository due to its size.

---

## 🖼️ Image Enhancement Pipeline

The following enhancement techniques are applied sequentially:

```text
Original Image
      ↓
Median Filtering
      ↓
Histogram Equalization
      ↓
Contrast Stretching
      ↓
High-Boost Filtering
      ↓
Gamma Correction
      ↓
Enhanced Image
```

### Techniques Used

**1. Median Filtering**
Used to reduce noise while preserving important image structures.

**2. Histogram Equalization**
Improves image contrast by redistributing intensity values.

**3. Contrast Stretching**
Expands the intensity range to improve overall contrast.

**4. High-Boost Filtering**
Enhances edges and important facial details.

**5. Gamma Correction**
Adjusts image brightness and improves visibility under different illumination conditions.

---

## 🧠 Model

A Convolutional Neural Network (CNN) is used for facial recognition.

The CNN architecture consists of:

* Conv2D — 32 filters
* MaxPooling
* Conv2D — 64 filters
* MaxPooling
* Flatten
* Dense — 128 neurons
* Softmax output layer

### Input Processing

* Images are converted to grayscale.
* Images are resized to **128 × 128**.
* Pixel values are rescaled to the range **[0, 1]**.

The model is trained for **10 epochs** using the Adam optimizer.

---

## 📊 Results

The experiments demonstrate an improvement in facial recognition performance after applying the image enhancement pipeline.

| Experiment         |  Accuracy |
| ------------------ | --------: |
| Before Enhancement |       85% |
| After Enhancement  | **97.1%** |

The best-performing random seed was **16**.

Across the tested seeds, the average accuracy after optimization was approximately **96.08% ± 1.08**.

The repository also includes visual evaluation such as:

* Confusion matrices
* Classification report
* Training and validation accuracy
* Training and validation loss
* Original vs. enhanced images
* Histogram comparisons

---

## 📓 Notebooks

### `Prepare_Data.ipynb`

Contains the dataset preparation workflow, including:

* Dataset extraction
* Organizing images by individual/class
* Dataset verification
* Checking image counts
* Checking image resolutions

### `Enhancement_and_CNN.ipynb`

Contains the main image enhancement and model workflow, including:

* Image enhancement
* Creating before/after datasets
* CNN training
* Model evaluation
* Confusion matrix
* Classification report
* Accuracy and loss curves
* Model saving

---

## ▶️ How to Run

The notebooks were developed and tested using **Google Colab** and **Google Drive**.

To run the notebooks from the beginning:

1. Download the required dataset.
2. Upload the dataset to Google Drive.
3. Open the notebook in Google Colab.
4. Mount Google Drive.
5. Update the dataset paths if necessary.
6. Run the notebook cells in order.

Example:

```python
from google.colab import drive
drive.mount('/content/drive')
```

> **Important:** The dataset is not included in this repository. The dataset paths used in the notebooks refer to directories stored in Google Drive.

---

## 🛠️ Technologies & Libraries

* Python
* Google Colab
* OpenCV
* NumPy
* Matplotlib
* PyTorch
* TensorFlow / Keras
* Scikit-learn
* Seaborn
* PIL

---

## 📁 Repository Structure

```text
face-recognition-image-enhancement/
│
├── README.md
├── Prepare_Data.ipynb
├── Enhancement_and_CNN.ipynb
│
├── results/
│   ├── original_vs_enhanced.png
│   ├── confusion_matrix_before.png
│   ├── confusion_matrix_after.png
│   └── accuracy_comparison.png
│
└── paper/
    └── research_paper.pdf
```

*The `results/` and `paper/` folders will be added to the repository.*

---

## 📄 Publication

This project was presented as a research paper:

**"Enhancing Facial Recognition Accuracy Through Image Processing Techniques"**

Authors: **Rowida Morsy, Tamer M. Nassef**

Published in the proceedings of **ICCA 2025**.

---

## 👩‍💻 Author

**Rowida Morsy**
Computer Science Student | Machine Learning & Computer Vision Enthusiast
