# Mars Surface Image Clustering with CNN Features

**Subhankar Tripathi** | EEN1083/EEN1085 — Dublin City University, 2024

Unsupervised analysis of the [NASA Mars Surface Image Dataset](https://www.kaggle.com/datasets/brsdincer/mars-surface-image-classif-curiosity-v2): 6,691 labelled images from the Curiosity rover across 25 surface categories. The labels describe the source dataset; the shipped notebook does not train a supervised multi-class classifier.

## Approach

The shipped notebook implements:
- **Frozen EfficientNetB0 CNN feature extraction** — generates image embeddings without training a new classifier
- **PCA dimensionality reduction** — reduces the embeddings to 50 components
- **Unsupervised K-Means clustering** — groups the PCA-reduced features without using category labels as training targets

## Results

K-Means on PCA-reduced CNN features produces groupings for distinct surface types such as drill, wheels, and horizon. Categories with visual similarity (for example, ground and observation tray) overlap. The observed silhouette-score range is 0.12–0.15, indicating limited cluster separation rather than classifier accuracy.

See the [project case study](https://www.subhankartripathi.com/projects/mars-surface-classification/) for additional context.

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

---

*Full portfolio: [subhankartripathi.com](https://www.subhankartripathi.com/)*
