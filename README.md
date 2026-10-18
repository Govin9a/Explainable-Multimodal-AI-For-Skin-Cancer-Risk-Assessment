# Explainable Multimodal AI for Skin Cancer Risk Assessment
Pilot study: do age, sex and lesion site add to lesion images for malignant-vs-benign risk assessment?
Image-only vs multimodal comparison, subgroup and calibration audits, Grad-CAM explanations.

## Data
MILK10k (CC BY-NC), obtained from the ISIC Archive. Images are not included here.
Tschandl P, et al. MILK10k: A Hierarchical Multimodal Imaging-Learning Toolkit for Diagnosing
Pigmented and Nonpigmented Skin Cancer and its Simulators. J Invest Dermatol. 2026;146(2):357-364.e7.
doi: 10.1016/j.jid.2025.06.1594.

## Run
Python 3.11/3.12, TensorFlow 2.16. Put the MILK10k files in a `data/` folder next to the notebook,
then run `Skin Cancer.ipynb` top to bottom.

## Note
Research prototype for risk-stratification support. Not a diagnostic device.
