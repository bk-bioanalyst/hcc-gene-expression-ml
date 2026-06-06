# 🧬 TCGA-LIHC Hepatocellular Carcinoma Classification using Machine Learning

> RNA-Seq Gene Expression Analysis, Cancer Classification, and Biological Interpretation using Explainable AI

---

## 📖 Project Overview

Hepatocellular Carcinoma (HCC) is the most common primary liver cancer and one of the leading causes of cancer-related deaths worldwide.

This project investigates whether transcriptomic (RNA-Seq) gene expression profiles can accurately distinguish HCC tumour samples from normal liver tissue using machine learning.

Using TCGA-LIHC RNA-Seq data containing 19,938 genes across 419 samples, multiple classification models were evaluated and biologically interpreted using SHAP explainability analysis.

---

## 🎯 Objectives

- Explore RNA-Seq gene expression patterns in HCC
- Perform exploratory data analysis (EDA)
- Build machine learning classifiers for tumour detection
- Compare model performance
- Identify biologically relevant biomarkers
- Interpret predictions using SHAP explainable AI

---

## 📊 Dataset

**Source:** The Cancer Genome Atlas (TCGA-LIHC)

| Parameter | Value |
|------------|---------|
| Samples | 419 |
| Genes | 19,938 |
| Cancer Type | Hepatocellular Carcinoma (LIHC) |
| Classification Task | Tumour vs Normal |

### Class Distribution

| Class | Samples |
|---------|---------|
| Tumour | 374 |
| Normal | 50 |

---

## 🔬 Exploratory Data Analysis

### Key Findings

- Significant class imbalance (~7.5:1)
- RNA-Seq counts showed strong right-skewed distribution
- Log₂(x+1) transformation improved data distribution
- PCA revealed clear separation between tumour and normal samples
- Tumour samples displayed greater transcriptomic heterogeneity

---

## ⚙️ Machine Learning Pipeline

```text
RNA-Seq Expression Matrix
            ↓
Data Cleaning
            ↓
Log2(x+1) Transformation
            ↓
Feature Standardization
            ↓
Train/Test Split (80/20)
            ↓
Model Training
   ├─ Logistic Regression
   └─ Linear SVM
            ↓
Cross Validation
            ↓
Performance Evaluation
            ↓
SHAP Interpretation
```

---

## 🤖 Models Evaluated

### Logistic Regression

- Class Weight: Balanced
- Stratified 10-Fold Cross Validation
- Probability Output Enabled
- SHAP Compatible

### Linear Support Vector Machine (LinearSVC)

- Class Weight: Balanced
- Linear Kernel
- High-dimensional genomic classification

---

## 📈 Results

### Logistic Regression (Best Model)

| Metric | Score |
|----------|----------|
| Accuracy | 97.62% |
| Balanced Accuracy | 98.65% |
| Precision | 100.00% |
| Recall | 97.30% |
| F1 Score | 98.63% |
| ROC-AUC | 1.000 |

### Linear SVM

| Metric | Score |
|----------|----------|
| Balanced Accuracy | 94.10% |
| F1 Score | 93.65% |

---

## 🏆 Selected Model

**Logistic Regression**

Selected because it demonstrated:

- Highest balanced accuracy
- Highest F1 score
- Superior recall
- Excellent generalization
- Probability calibration
- Biological interpretability

---

## 🧠 Explainable AI (SHAP)

SHAP analysis was performed to identify genes contributing most strongly to tumour classification.

### Top Biologically Relevant Genes

| Gene | Biological Role |
|--------|----------------|
| EDIL3 | EMT and angiogenesis |
| SLC5A8 | Tumour suppressor |
| IFNA8 | Immune signalling |
| KIR3DL3 | Immune evasion |
| GDF1 | Metastasis and tumour progression |
| RNASE1 | Vascular remodelling |

---

## 🧬 Biological Insights

The classifier captured multiple hallmarks of cancer:

### EMT and Invasion
- EDIL3
- GDF1

### Angiogenesis and Tumour Vasculature
- RNASE1
- VWF
- CAPN11

### Immune Dysregulation
- IFNA8
- KIR3DL3

### Tumour Suppression and Wnt Signalling
- SLC5A8

These findings align with established molecular mechanisms of hepatocellular carcinoma.

---

## 📂 Repository Structure

```text
tcga-lihc-hcc-classification/

├── data/
├── notebooks/
├── src/
├── figures/
├── results/
├── README.md
├── requirements.txt
└── LICENSE
```

---

## 🛠 Tools & Technologies

### Programming

- Python

### Data Analysis

- Pandas
- NumPy

### Machine Learning

- Scikit-learn

### Visualization

- Matplotlib
- Seaborn

### Explainable AI

- SHAP

---

## 🚀 Future Improvements

- Random Forest comparison
- XGBoost implementation
- Feature selection pipeline
- External validation datasets
- Biomarker prioritization
- Survival prediction modelling

---

## 👩‍🔬 Author

**Barsha Rani Kar**

M.Tech Computational Biology

Bioinformatics | Machine Learning | Cancer Genomics

🔗 LinkedIn:
linkedin.com/in/barsharanikar

---

## ⭐ Project Highlights

✅ 419 TCGA samples

✅ 19,938 RNA-Seq genes

✅ 98.65% Balanced Accuracy

✅ ROC-AUC = 1.00

✅ SHAP-based biological interpretation

✅ Cancer biomarker discovery workflow
