# Emtensor_Priyanshujha
This project implements a brain MRI segmentation and anomaly detection pipeline. It processes neuroimaging data, applies data augmentation, trains a 3D U-Net segmentation model, performs inference, and visualizes results. The anomaly detection module utilizes attention mechanisms for improved analysis.

Features

✅ Preprocessing: Loads and normalizes NIfTI brain scans.
✅ Data Augmentation: Applies affine transformations (rotation & translation).
✅ Segmentation Model: Uses a 3D U-Net for multi-class segmentation.
✅ Anomaly Detection: Attention-based mechanism for detecting anomalies.
✅ Inference: Monte Carlo Dropout for uncertainty estimation.
✅ Visualization: Heatmaps and 3D slice visualization.



# Install dependencies
pip install -r requirements.txt

Run the entire pipeline with:

python main.py

This will:

Preprocess the brain MRI scan.

Apply data augmentation.

Run segmentation using a 3D U-Net.

Perform anomaly detection.

Estimate uncertainty using Monte Carlo Dropout.

Conduct statistical analysis (t-tests, ANOVA).

Generate heatmaps and 3D visualizations.

File Descriptions

1. Preprocessing (preprocess.py)

Loads NIfTI brain scans (.nii files).

Normalizes intensity values to [0, 1].

Pads images to the nearest multiple of 16.

2. Data Augmentation (augmentation.py)

Applies random affine transformations (rotation & translation).

3. Segmentation Model (segmentation_model.py)

Defines a 3D U-Net model for multi-class brain tissue segmentation:

Gray Matter, White Matter, Ventricles, Hippocampus

4. Anomaly Detection (anomaly_detection.py)

Uses attention gates with 3D convolutions for detecting anomalies.

5. Inference & Uncertainty Estimation (inference.py)

Runs segmentation inference.

Uses Monte Carlo Dropout to estimate uncertainty.

6. Statistical Analysis (sacode.py)

Performs t-tests and ANOVA for segmentation analysis.

7. Visualization (visualize.py)

Generates heatmaps of segmentation results.

Plots 3D slice views of MRI scans.

Example Output

Segmentation Heatmap



3D MRI Slices

