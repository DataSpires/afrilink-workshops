
# AfriLink Computer Vision Tutorial

**Breast cancer lesion detection with YOLOv8, from prototype to HPC.**

This notebook is a self-contained walkthrough built for the Africa AI Olympiad. It takes you from raw mammography data to a trained object detection model, using Kaggle GPUs for fast iteration and CINECA A100 nodes (via the AfriLink SDK) for full-scale training.

## What it covers

| Section | What happens |
|---------|-------------|
| 0 | Setup — installs, dataset verification, GPU check |
| 1 | Data exploration — annotation distribution, bounding box analysis, sample visualisation |
| 2 | Dataset preparation — BI-RADS filtering, YOLO-format label conversion, train/val split |
| 3 | Baseline — YOLOv8 nano quick sanity check on a 2k-image subset |
| 4 | Improved model — YOLOv8 small with medical-aware augmentation (CLAHE, rotation, mosaic) |
| 5 | Evaluation — precision/recall, per-class mAP, prediction overlays, loss curves |
| 6 | HPC scale-up — authenticate with AfriLink, upload dataset, submit full training job to A100s, monitor, download weights |

## Dataset

[VinDr-Mammo PNG edition](https://www.kaggle.com/datasets/shantanughosh/vindr-mammogram-dataset-dicom-to-png) — pre-converted mammography PNGs with bounding box annotations across BI-RADS severity levels. The notebook simplifies to a binary task: **benign** vs **malignant**.

## Requirements

- **Sections 0-5**: Kaggle GPU (T4/P100) — no account needed
- **Section 6**: A [DataSpires](https://dataspires.com) account and `pip install afrilink-sdk` for HPC job submission
