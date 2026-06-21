# Multimodal classification with SigLIP embeddings

A 200-class image classifier on ~10,000 samples built on pre-computed SigLIP
vision–language embeddings, plus a cross-modal analysis of how the image and
caption representations align.

## What it does
- **Classify:** train and tune an `MLPClassifier` — hidden-layer architecture
  selected via 3-fold `GridSearchCV` on F1-macro — reaching **F1-macro ≈ 0.58**.
- **Cross-modal analysis:** run 200-cluster KMeans separately on the image and
  caption embedding spaces and compute the **Adjusted Rand Index** to quantify
  how well the two modalities agree.

## Stack
Python, scikit-learn (MLPClassifier, KMeans, GridSearchCV), NumPy.

## Files
- `multimodal_siglip.ipynb` — the notebook (embeddings → tuning → evaluation → cross-modal analysis).
