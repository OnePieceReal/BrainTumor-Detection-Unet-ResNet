# Brain Tumor Segmentation and Classification

## Table of Contents
1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Results](#results)
4. [Evaluation Metrics](#evaluation-metrics)

---

## Introduction

This project presents a deep learning pipeline for automated brain tumor detection and classification, integrating both segmentation and classification tasks to enhance tumor analysis. A U-Net architecture is employed to segment tumor regions from T1-weighted MRI scans by producing binary masks that localize tumor areas. For classification, a fine-tuned ResNet-50 model categorizes the detected tumors into three classes: meningioma, glioma, and pituitary. 

The models were trained and evaluated on a publicly available dataset annotated for both segmentation and classification, ensuring consistency and reliability in performance assessment. Additionally, the `ML_Algorithms` folder contains machine learning algorithms implemented from scratch, including Linear Regression, Logistic Regression, clustering algorithms (DBSCAN, K-means, Nearest Neighbor), and a neural network solution for the XOR problem.

---

## Dataset

The dataset consists of 3,064 brain MRI scans, each annotated with a patient ID, MRI image, tumor type, segmentation mask, and tumor boundary. To ensure a robust evaluation, the dataset was split into training, validation, and test sets with no patient overlap across splits. This prevents data leakage, as some patients have multiple MRI scans, and ensures that model performance reflects true generalization.

**Dataset Download Link**: [Brain Tumor Dataset - Papers with Code](https://paperswithcode.com/dataset/brain-tumor-dataset)  

### Distribution of Tumor Types in Dataset  

| Tumor Type | Num of Samples | Percentage |
|------------|----------------|------------|
| Meningioma | 708            | 23.1%      |
| Glioma     | 1,426          | 46.5%      |
| Pituitary  | 930            | 30.4%      |

---

## Results  

The segmentation and classification models demonstrate strong performance, as shown below:  

<p align="center">
  <strong>Figure 1: Segmentation and Classification Outputs</strong><br>
  <img src="Results/result_1.PNG" width="80%"><br>
  <img src="Results/result_2.PNG" width="80%">
</p>

---

## Evaluation Metrics  

The models were evaluated on the test set using the following metrics:  

- **Dice Score (Segmentation)**: 0.7495  
- **Accuracy (Classification)**: 96%  

<p align="center">
  <strong>Figure 2: Confusion Matrix for Classification</strong><br>
  <img src="Results/confusion_matrix.PNG" width="60%">
</p>  

<p align="center">
  <strong>Figure 3: Accuracy and Dice Score Over Time</strong><br>
  <img src="Results/accuracy_dice_over_time.PNG" width="60%">
</p>  

<p align="center">
  <strong>Figure 4: Training and Validation Loss Over Time</strong><br>
  <img src="Results/loss_over_time.PNG" width="60%">
</p>
