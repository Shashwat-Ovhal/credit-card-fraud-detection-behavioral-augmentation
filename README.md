# 💳 Credit Card Fraud Detection with Behavioral Augmentation and Interpretable Models

### 📄 Overview
This repository contains the implementation and research artifacts for the paper  
**"Credit Card Fraud Detection with Behavioral Augmentation and Interpretable Models"**  
authored by **Shashwat Sambhaji Ovhal** and **Sumit Shivaji Satpute**, Department of Electrical and Electronics Engineering, MIT-WPU, Pune, India.

This project proposes a fraud detection framework that integrates **behavioral user features** (e.g., login hour, session count, device change count) with traditional transaction data and focuses on **model interpretability** using **SHAP (SHapley Additive exPlanations)**.

---

### 🧠 Abstract
> Credit card fraud is a critical concern for financial institutions and consumers alike, demanding accurate yet transparent detection models.  
> This study proposes an enhanced fraud detection framework that integrates behavioral features with traditional transaction data and emphasizes model interpretability via SHAP.  
> Using the public Kaggle credit card dataset (284,807 transactions, 0.172% fraud), we synthesize behavioral attributes such as login hour, session count, and device change count.  
> A Random Forest classifier trained on this enriched dataset achieves **~99.95% accuracy** and **AUC ≈ 0.957**, while improving recall for fraud cases.  
> SHAP analysis reveals which behavioral and transaction features drive the model’s decisions, demonstrating that **behavior-aware, interpretable AI** offers both transparency and accuracy.

---

### 🧩 Key Features
- Combines **transactional** and **behavioral** data for fraud detection  
- Implements **Random Forest classifier** with and without **SMOTE oversampling**  
- **SHAP-based interpretability** for feature importance and transparency  
- Achieves **AUC ≈ 0.957**, **accuracy ≈ 99.95%**, **recall up to 0.84**  
- Complete, reproducible Jupyter Notebook  

---

### 🧰 Requirements

Install dependencies using:

```bash
pip install -r requirements.txt
