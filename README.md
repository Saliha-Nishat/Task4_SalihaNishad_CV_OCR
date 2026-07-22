## 📌 Short Repo Description

> A Computer Vision and OCR pipeline built with OpenCV and PyTesseract in Python. Ingests raw visual data, applies systematic image pre-processing (Grayscale, Gaussian Blur, Otsu's Adaptive Thresholding), extracts machine-readable text, and enforces an 80% confidence gatekeeper rule with bounding box visualization. Developed as part of the DecodeLabs AI Industrial Training Program (Batch 2026).

---

## 📄 `README.md` File

Copy and paste the markdown below directly into your repository's `README.md` file:

```markdown
# DecodeLabs AI Industrial Training: Project 4 – Image & Text Recognition

![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)
![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-green.svg)
![Tesseract](https://img.shields.io/badge/Tesseract-OCR%20Engine-orange.svg)
![Status](https://img.shields.io/badge/Milestone-PASSED%20(95.11%25)-brightgreen.svg)

## 📌 Overview
This project implements an end-to-end **Optical Character Recognition (OCR)** pipeline as part of the **DecodeLabs AI Industrial Training Program (Batch 2026)**. 

The pipeline bridges unstructured visual data and computational logic by ingesting raw images, applying systematic pre-processing to eliminate noise and chromatic artifacts, extracting text, and benchmarking model accuracy against a strict **80% confidence gatekeeper standard**.

---

## 🚀 Key Features & Workflow

The recognition pipeline follows the **Input-Processing-Output (IPO)** architectural model:

1. **Systematic Pre-Processing Pipeline:**
   * **Grayscale Conversion:** Collapses 3D RGB channels into a 1D intensity matrix to strip unnecessary color noise.
   * **Gaussian Blur:** Smooths micro-imperfections and high-frequency noise.
   * **Otsu's Adaptive Thresholding:** Dynamically calculates optimal cutoffs to transform grayscale inputs into crisp, high-contrast binary matrices.

2. **Model Inference & Benchmarking:**
   * Leverages Google's pre-trained **Tesseract OCR engine** (`pytesseract`) configured with tuned Page Segmentation Modes (PSM).
   * Extracts pixel-level bounding coordinates and word-level confidence scores.

3. **Gatekeeper Filtering & Visual Confirmation:**
   * Enforces a mandatory **$\ge 80\%$ confidence threshold** to eliminate false positives and hallucinations.
   * Overlays precise green bounding boxes (`cv2.rectangle`) around validated text entities.
   * Generates a 3-panel side-by-side visual comparison (*Original $\rightarrow$ Pre-processed Binary $\rightarrow$ Bounding Boxes*).

---

## 🛠️ Tech Stack & Requirements

* **Environment:** Google Colab / Python 3.x
* **Core Libraries:**
  * `opencv-python-headless` (Computer Vision Operations)
  * `pytesseract` (Python wrapper for Tesseract-OCR)
  * `numpy` (Matrix manipulations)
  * `matplotlib` (Inline visualization)

---

## ⚡ Quickstart Guide (Google Colab)

### 1. Install Dependencies
```bash
!apt-get update -qq && apt-get install -y tesseract-ocr
!pip install pytesseract pillow matplotlib opencv-python-headless

```

### 2. Run the Pipeline

1. Clone or open `Project_4_OCR.ipynb` in Google Colab.
2. Upload your target image file when prompted.
3. Execute all cells to view the 3-panel visual output and validation summary report.

---

## 📊 Sample Output & Milestone Validation

```text
==================================================
              MILESTONE VALIDATION REPORT            
==================================================
Extracted Text String : Fellows & champions For successfully completing the fellowship program!
Average Confidence   : 95.11%
Gatekeeper Rule      : PASSED (>= 80% standard met)
==================================================

```

### Validation Checklist

* [x] **Library Integration:** Error-free execution of OpenCV and PyTesseract.
* [x] **Pre-Processing Integrity:** Demonstrable execution of Grayscale and Otsu Thresholding.
* [x] **Accuracy Benchmarking:** Validated average confidence score exceeding the 80% minimum standard (Achieved: **95.11%**).
* [x] **Visual Confirmation:** Generation of side-by-side visual output with clear text bounding boxes.

---

## 👤 Author

* **Developer:** Saliha Nishad Farid
* **Program:** DecodeLabs Artificial Intelligence Industrial Training (Batch 2026)

```

```
