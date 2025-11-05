<!-- ───────────────────────────────────────────── -->
<!-- ✨ CREDIT CARD FRAUD DETECTION README ✨ -->
<!-- ───────────────────────────────────────────── -->

<div align="center">

# 💳 Credit Card Fraud Detection  
### with Behavioral Augmentation and Interpretable Models

**Authors:** Shashwat Sambhaji Ovhal & Sumit Shivaji Satpute  
_Department of Electrical and Electronics Engineering, MIT-WPU, Pune, India_

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-%3E=1.3-orange.svg)](https://scikit-learn.org/)
[![Paper DOI](https://img.shields.io/badge/IJSRST-Vol.12%2C%20Issue%2017-green)](https://ijsrst.com/home/issue/view/article.php?id=IJSRST25121746)

---

> **Abstract:**  
> This research proposes a behavior-aware fraud detection framework integrating *transactional* and *user-behavioral* features with interpretable ML models.  
> A Random Forest trained on the Kaggle credit-card dataset (284 807 transactions, 0.172 % fraud) achieved  
> **≈ 99.95 % accuracy**, **AUC ≈ 0.957**, and **recall ≈ 0.84** after behavioral augmentation and SHAP-based explainability.

</div>

---

## 📖 Table of Contents
1. [Overview](#-overview)
2. [Dataset](#-dataset)
3. [Methodology](#-methodology)
4. [Results & Performance](#-results--performance)
5. [Key Features](#-key-features)
6. [Project Structure](#-project-structure)
7. [Installation](#-installation)
8. [How to Run](#-how-to-run)
9. [Interpretability (SHAP)](#-interpretability-shap)
10. [Conclusion](#-conclusion)
11. [How to Cite](#-how-to-cite)
12. [License](#-license)

---

## 🧠 Overview
Fraud detection demands both *accuracy* and *explainability*.  
This project enriches traditional transaction data with **behavioral features** such as:
- Login hour  
- Session count (24 h window)  
- Device change count  
- Device-type indicators  

A **Random Forest Classifier** (with and without **SMOTE**) was trained on this enriched dataset.  
Interpretability is achieved through **SHAP (SHapley Additive Explanations)** to reveal feature-level influence.

---

## 📊 Dataset
- **Source:** [Kaggle – Credit Card Fraud Detection Dataset (2018)](https://www.kaggle.com/mlg-ulb/creditcardfraud)  
- **Records:** 284 807 transactions  
- **Fraud Cases:** 492 (≈ 0.172 %)  
- **Features:** 28 PCA components + Amount + Time + behavioral features

---

## ⚙️ Methodology
| Step | Description |
|------|--------------|
| **1. Data Augmentation** | Simulated behavioral signals (login hour, session count, device change count). |
| **2. Pre-processing** | Scaling (`StandardScaler`) and label encoding. |
| **3. Model Training** | `RandomForestClassifier(n_estimators=200, class_weight='balanced')`. |
| **4. Oversampling** | Optional **SMOTE** for minority-class balancing. |
| **5. Evaluation Metrics** | Accuracy, Recall, Precision, F1, ROC AUC. |
| **6. Explainability** | **SHAP TreeExplainer** for global & local feature importance. |

---

## 🧩 Key Features
✅ Behavioral + transactional data  
✅ SMOTE oversampling support  
✅ Explainable AI via SHAP  
✅ Reproducible Jupyter Notebook  
✅ High AUC and recall on imbalanced data  

---

## 📈 Results & Performance
| Metric | Score |
|---------|-------|
| **Accuracy** | 99.95 % |
| **AUC** | 0.957 |
| **Recall (fraud)** | 0.84 |
| **Precision (fraud)** | 0.96 |

<div align="center">

| ROC Curve | SHAP Summary | Top Features |
|:--:|:--:|:--:|
| ![ROC Curve](Results%20and%20Performance/ROC_Curve.png) | ![SHAP Outputs](Results%20and%20Performance/SHAP_outputs.png) | ![Top Features](Results%20and%20Performance/Top-20_feature_Importances.png) |

</div>

---

## 🗂️ Project Structure
```bash
CREDIT-CARD-FRAUD-DETECTION/
│
├── Notebook/
│   ├── Credit_Card_Fraud__Detection.ipynb
│   ├── creditcard.csv
│   ├── rf_fraud_model.joblib
│   └── scaler_Time_Amount.joblib
│
├── Research Paper/
│   ├── Credit Card Fraud Detection with Behavioral Augmentation and Interpretable Models.pdf
│   └── Journal_link.txt
│
├── Results and Performance/
│   ├── ROC_Curve.png
│   ├── SHAP_outputs.png
│   └── Top-20_feature_Importances.png
│
├── CITATION.cff
├── LICENSE
├── README.md
└── requirements.txt

## 📝 How to Cite

If you use this work, please cite the following publication:

Shashwat Sambhaji Ovhal & Sumit Shivaji Satpute.
Credit Card Fraud Detection with Behavioral Augmentation and Interpretable Models.
International Journal of Scientific Research in Science and Technology (IJSRST), Vol. 12 Issue 17 (2025).
Read online here → IJSRST 25121746
@article{Ovhal2025CreditCardFraud,
  title   = {Credit Card Fraud Detection with Behavioral Augmentation and Interpretable Models},
  author  = {Ovhal, Shashwat Sambhaji and Satpute, Sumit Shivaji},
  journal = {International Journal of Scientific Research in Science and Technology},
  year    = {2025},
  volume  = {12},
  number  = {17},
  pages   = {307--314},
  url     = {https://ijsrst.com/home/issue/view/article.php?id=IJSRST25121746}
}

##📄 License

This project is licensed under the MIT License — see LICENSE.
---

<div align="center">

⭐ If you find this repository useful, please give it a star on GitHub! ⭐

</div> ```