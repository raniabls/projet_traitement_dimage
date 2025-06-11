# 💰 Coin Detection and Counting - Image Processing Project

## 📌 Description

This project focuses on the **automated detection, counting, and classification of coins** using advanced **digital image processing** techniques. Developed as part of the **Image Processing module** in the Master's ISII program at Université d'Alger 1, the goal is to recognize coins in an image, count them accurately, and differentiate them by size — which may reflect their denomination.

The final system integrates a **graphical interface** (Tkinter) to allow users to upload an image and visualize both the processing steps and results.

---

## 🎯 Objectives

- ⚙️ Preprocess input coin images to enhance contrast and remove noise
- ✂️ Segment the image to isolate coins using Otsu’s thresholding
- 🔍 Apply morphological operations to clean segmentation results
- 🔢 Detect and count coins using connected component labeling (DFS)
- 📏 Classify coins by size (area-based thresholds)
- 🖥️ Develop a simple user interface for interaction

---

## 🧠 Methodology

### 🖼️ 1. Image Preprocessing
- **Contrast Adjustment**
- **Histogram Equalization**
- **Log and Power Transformations**
- **Smoothing Filters** (Median and Mean)

> Best results were obtained using histogram equalization and smoothing.

### 🧱 2. Segmentation
- Applied **Otsu's method** for automatic binary thresholding.

### 🧬 3. Morphological Processing
- Used **Opening + Closing** operations to clean the binary image.
- Improved the accuracy of shape-based counting.

### 🔄 4. Object Counting
- Used a **Depth-First Search (DFS)** algorithm for connected component labeling.
- Counted only white-pixel regions (value = 255) representing coins.

### 🧩 5. Classification by Size
- Based on pixel area:
  - **Small Coin**: area < 200 px
  - **Medium Coin**: 200 ≤ area < 800 px
  - **Large Coin**: area ≥ 800 px

### 🖼️ 6. GUI Interface (Tkinter)
- Upload and display input image
- Run the full processing pipeline
- Show results: segmented image and coin count

---

## 🧰 Tech Stack

| Component         | Technology        |
|------------------|-------------------|
| Language          | Python            |
| Libraries         | OpenCV, NumPy, Tkinter |
| Processing Tools  | Custom filtering, Otsu Thresholding, DFS |
| GUI               | Tkinter (Python GUI toolkit) |

---

## 📊 Evaluation

The model’s performance was evaluated based on **counting accuracy**:
- Results were recorded in Excel
- Performance slightly drops with noisy images, but size-based classification helps preserve interpretation accuracy

