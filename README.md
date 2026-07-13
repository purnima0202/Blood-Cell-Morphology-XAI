# Blood-Cell-Morphology-XAI
Every prediction is transparent, auditable, and explainable — with counterfactual reasoning ("this cell would be normal if the nucleus were 23% smaller").

---

## 🛠️ What I Built

**Computer Vision** — Training-free cell segmentation (nucleus, cytoplasm, whole cell) using CMYK/HLS colour space transformations and Otsu thresholding, following Tarquino et al. (2024).

**Feature Engineering** — Extracted **84 features per cell** across 3 regions: shape (area, solidity, roundness), colour (RGB channel statistics), and texture (GLCM contrast, entropy).

**Quality Pipeline** — Automated single-cell filtering using connected-component analysis; reproducible dataset construction with fixed random seed.

**Classification** *(in progress)* — SVM baseline, ResNet-18 deep learning baseline, and interpretable SGE classifier.

---

## 📊 Dataset

Matek et al. (2021) Bone Marrow Cytomorphology — 171,374 expert-annotated images.

| Class | Type | Role |
|-------|------|------|
| BLA | 🔴 Malignant | Blast cells (leukaemia indicator) |
| NGS | 🟢 Normal | Segmented neutrophils |
| LYT | 🟢 Normal | Lymphocytes |

Working set: **3,000 quality-filtered images** (1,000 per class).

---

## ✅ Progress

- [x] Data pipeline — download, filter, reproducible sampling
- [x] Cell segmentation (3 regions)
- [x] Feature extraction — 84 features → `metadata.csv`
- [ ] SVM & ResNet-18 baselines
- [ ] SGE interpretable classifier
- [ ] Counterfactual explanation module
- [ ] Streamlit prototype

---

## 💻 Tech Stack

`Python` · `OpenCV` · `scikit-image` · `scikit-learn` · `PyTorch` · `sge3` · `Streamlit`

---

## 🚀 Run It

1. Open `01_Data_Preparation_And_Feature_Extraction.ipynb` in Google Colab
2. Add your `kaggle.json` API key
3. Run all → `metadata.csv` generated

---

## 📚 References

Tarquino et al. (2024), *J. Pathology Informatics* · Matek et al. (2021), *Blood* · Lourenço et al. (2016), *Genetic Programming and Evolvable Machines*
