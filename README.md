# Workshops

Notebooks that demonstrate the AfriLink SDK across different problem domains. Each one is a standalone tutorial you can run on Colab, Kaggle, or any Jupyter environment.

| Notebook | Domain | What it does |
|----------|--------|-------------|
| [AfriLink Computer Vision Tutorial](AfriLink%20Computer%20Vision%20Tutorial.ipynb) | Medical Imaging | YOLOv8 breast cancer lesion detection — prototype on Kaggle GPUs, scale to A100s via `client.train()`. [Read more](CV_TUTORIAL_README.md) |

## Getting started

```bash
pip install afrilink-sdk
```

All notebooks assume a [DataSpires](https://dataspires.com) account for HPC sections, and can be copied and customised for any varied usecase that relies on the SDK. Local/Kaggle GPU sections run independently.
