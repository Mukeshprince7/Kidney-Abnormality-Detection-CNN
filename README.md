# Kidney Abnormality Detection from CT

## Problem Statement
**PS No.: 21 — Image Classification Challenge**

A deep learning project that classifies kidney CT images into four categories: Cyst, Normal, Stone, and Tumor.

## Project Details
- **Student:** Mukesh T
- **Register Number:** RA2311026050205
- **Section:** AIML - A
- **Framework:** TensorFlow / Keras
- **Architecture:** MobileNetV2 transfer learning
- **Input Image Size:** 224 × 224
- **Number of Classes:** 4

## Dataset
The project uses the CT Kidney Dataset available on Kaggle.

Dataset link: https://www.kaggle.com/datasets/nazmul0087/ct-kidney-dataset-normal-cyst-tumor-and-stone

Classes:
- Cyst
- Normal
- Stone
- Tumor

The dataset contains 12,446 images, divided into training (8,712), validation (1,867), and test (1,867) sets.

## Methodology
1. Load and inspect the CT images.
2. Split the dataset using stratified image-level splitting.
3. Resize images to 224 × 224 and apply MobileNetV2 preprocessing.
4. Use pretrained ImageNet weights with a frozen MobileNetV2 backbone.
5. Train the classification head using Adam and class weights.
6. Evaluate the model using test accuracy, precision, recall, F1-score, and a confusion matrix.

## Results
- **Test Accuracy:** 95.66%
- **Macro F1-score:** 0.94
- **Stone Recall:** 92.27%

| Class | Precision | Recall | F1-score |
|---|---:|---:|---:|
| Cyst | 0.98 | 0.96 | 0.97 |
| Normal | 0.99 | 0.96 | 0.97 |
| Stone | 0.88 | 0.92 | 0.90 |
| Tumor | 0.91 | 0.96 | 0.93 |

## How to Run
1. Open `Kidney_Abnormality_CNN.ipynb` in Google Colab.
2. Download the dataset from Kaggle.
3. Upload or mount the dataset in Google Drive.
4. Update the dataset path to match your folder structure.
5. Run the notebook cells in order.

## Limitations
The evaluation uses an image-level split, so patient-level data leakage has not been ruled out. The model has not been externally validated and is not intended for clinical diagnosis.

## Disclaimer
This project is for academic and educational purposes only. Predictions must not be used as a substitute for professional medical evaluation.

