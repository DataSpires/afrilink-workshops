# Workshops

Notebooks that demonstrate the AfriLink SDK across different problem domains. Each one is a standalone tutorial you can run on Colab, Kaggle, or any Jupyter environment.

| Notebook | Domain | What it does |
|----------|--------|-------------|
| [AfriLink Computer Vision Tutorial](AfriLink%20Computer%20Vision%20Tutorial.ipynb) | Medical imaging | YOLOv8 breast cancer lesion detection — prototype on Kaggle GPUs, scale to A100s via `client.train()`. [Read more](computerVisionTutorial.md) |
| [Afrilink Context Engineering Tutorial](AfriLink%20Context%20Engineering%20Tutorial.ipynb) | NLP / RAG / Context engineering | Retrieval strategies for South African legal text, scaling from prompt-stuffing to HPC-backed semantic search. [Read more](contextEngineeringTutorial.md) |

## Getting started

```bash
pip install afrilink-sdk
```

All notebooks assume a [DataSpires](https://dataspires.com) account for HPC sections. Local/Kaggle GPU sections run independently.
