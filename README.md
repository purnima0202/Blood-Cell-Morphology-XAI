# Blood-Cell-Morphology-XAI
# Multimodal Explainable AI for Blood Cell Morphology Classification

Masters dissertation project — University of Limerick


## Project Overview
Building an interpretable AI system for bone marrow cell classification
using Structured Grammatical Evolution (SGE) and engineered image features.

## Dataset
Matek et al. (2021) Bone Marrow Cytomorphology Dataset
- 3 classes: BLA (blast/malignant), NGS (neutrophil/normal), LYT (lymphocyte/normal)
- 1000 images per class = 3000 total after quality filtering

## Current Progress
- [x] Dataset downloaded and filtered
- [x] Cell segmentation (nucleus, cytoplasm, whole cell)
- [x] Feature extraction — 84 features per cell
- [x] metadata.csv saved
- [ ] SVM baseline classifier
- [ ] ResNet-18 baseline
- [ ] SGE with BNF grammar
- [ ] Counterfactual explanation module
- [ ] Streamlit prototype

## Feature Extraction
Following Tarquino et al. (2024) — 84 features per cell:
- Shape features (8 per region)
- Colour features (15 per region)
- Texture/GLCM features (5 per region)
- 3 regions: whole cell, nucleus, cytoplasm

## Reference
Tarquino et al. (2024) Engineered feature embeddings meet deep learning.
Journal of Pathology Informatics 15, 100390.
