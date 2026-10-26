# Explainable Multimodal AI for Skin Cancer Risk Assessment

Pilot study: do age, sex and lesion site add to lesion images for malignant-vs-benign risk assessment?
Image-only vs multimodal comparison, subgroup and calibration audits, Grad-CAM explanations.

## Summary (one training run, held-out test lesions)
- Image only: AUC 0.83 (95% CI 0.80-0.86). Image + age, sex, site: AUC 0.84 (0.81-0.87).
  Paired AUC gain +0.007 (95% CI 0.000 to 0.014).
- At a validation-chosen threshold for 95% sensitivity: sensitivity 0.95, specificity 0.47, F1 0.88.
- Sensitivity was lower for darker skin tones (classes 0-2) and younger patients.

## Data
MILK10k (CC BY-NC), obtained from the ISIC Archive. The images are not included here;
the label and metadata CSV files are.

Tschandl P, et al. MILK10k: A Hierarchical Multimodal Imaging-Learning Toolkit for Diagnosing
Pigmented and Nonpigmented Skin Cancer and its Simulators. J Invest Dermatol. 2026;146(2):357-364.e7.
doi: 10.1016/j.jid.2025.06.1594.

## Run
Python 3.11/3.12, TensorFlow 2.16.
1. Download `MILK10k_Training_Input.zip` from the ISIC Archive and extract it to `MILK10k_Training_Input/`.
2. Put the three CSV files and the extracted folder in a `data/` folder next to the notebook.
3. Open `Skin Cancer.ipynb` and run it top to bottom.

## Note
Research prototype for risk-stratification support. Not a diagnostic device.
