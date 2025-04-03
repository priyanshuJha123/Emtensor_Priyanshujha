# Emtensor_Priyanshujha
Project Overview
This project implements a pipeline for brain MRI segmentation and anomaly detection. It processes neuroimaging data, applies data augmentation, trains a segmentation model, performs inference, and visualizes results. The segmentation model is based on a 3D U-Net, and the anomaly detection module utilizes attention mechanisms.

Directory Structure & File Descriptions
1. Preprocessing
preprocess.py

Loads and processes NIfTI brain scans.

Normalizes intensity values to [0, 1].

Pads images to dimensions that are multiples of 16.

2. Data Augmentation
augmentation.py

Applies random affine transformations (rotation and translation) to MRI images.

3. Segmentation Model
segmentation_model.py

Defines a 3D U-Net model for multi-class brain tissue segmentation (e.g., gray matter, white matter, ventricles, hippocampus).

4. Anomaly Detection
anomaly_detection.py

Implements an attention-based anomaly detection module that applies spatial attention using 3D convolutions.

5. Inference
inference.py

Runs inference using the segmentation model.

Supports Monte Carlo Dropout for uncertainty estimation.

6. Statistical Analysis
sacode.py

Performs t-tests and ANOVA for statistical comparison of segmented results.

7. Visualization
visualize.py

Generates heatmaps and 3D slices of segmentation outputs.

8. Main Pipeline
main.py

Integrates preprocessing, augmentation, segmentation, inference, statistical analysis, and visualization.

Pipeline Execution
Preprocessing

Load a NIfTI brain scan (.nii file).

Normalize intensities and pad the image.

Augmentation

Apply affine transformations to generate varied data.

Segmentation

Load the 3D U-Net model and segment brain structures.

Anomaly Detection

Apply attention mechanisms to highlight anomalies.

Inference & Uncertainty Estimation

Predict segmentation output.

Perform Monte Carlo Dropout for uncertainty quantification.

Statistical Analysis

Perform t-tests and ANOVA on segmented structures.

Visualization

Generate heatmaps and 3D slice views.

Usage
bash
Copy
Edit
python main.py
This runs the entire pipeline from preprocessing to visualization.

Summary
The project segments brain structures using a 3D U-Net.

It applies attention-based anomaly detection.

Supports uncertainty estimation via Monte Carlo Dropout.

Outputs statistical analysis and heatmaps of the segmentation results.

Let me know if you need modifications or additional details!
