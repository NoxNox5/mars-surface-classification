# Mars Surface Image Classification

**Subhankar Tripathi** | EEN1083/EEN1085 — Dublin City University, 2024

Multi-class image classification and unsupervised clustering on the [NASA Mars Surface Image Dataset](https://www.kaggle.com/datasets/brsdincer/mars-surface-image-classif-curiosity-v2) — 6,691 labelled images from the Curiosity rover across 25 surface categories.

## Approach

Two methods compared:
- **EfficientNetB0 feature extraction + K-Means clustering** (unsupervised)
- PCA dimensionality reduction (50 components) → cluster visualisation

## Results

K-Means on PCA-reduced CNN features produces meaningful groupings for distinct surface types (drill, wheels, horizon). Categories with visual similarity (e.g. ground vs observation tray) predictably overlap. Silhouette score ~0.12–0.15.

## Setup

```bash
pip install tensorflow pillow scikit-learn matplotlib seaborn pandas
```

Download dataset → extract to `data/Mars Surface Images Dataset/`  
Then run `notebooks/mars_surface_classification.ipynb`

## Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
