# 📬 SMS Spam Classification

This repository contains a machine learning project for **detecting spam SMS messages** using multiple classification algorithms.  
The goal is to compare the performance of different models — especially after feature scaling — and interpret their precision scores.

---

## 📁 Repository

**GitHub:** https://github.com/Abderaouf-KHELFAOUI/spam-classification.git

---

## 🧠 Project Overview

In this project, we:

- Loaded a publicly available SMS spam dataset.
- Scaling data
- Trained multiple machine learning models.
- Compared their precision scores with and without feature scaling.

This project demonstrates how preprocessing — especially feature scaling — influences model performance, particularly for distance- or margin-based algorithms.

---

## 📦 Dataset

We used the **SMS Spam Detection Dataset** from Kaggle:

🔗 https://www.kaggle.com/datasets/vishakhdapat/sms-spam-detection-dataset?utm_source=chatgpt.com

### Dataset Description

- Contains SMS text messages labeled as **spam** or **ham** (not spam).
- Ideal for binary text classification.
- Used for training and evaluating multiple models.

---

## 🔄 Preprocessing Steps
1. **Feature Scaling**
   - Applied scaling (e.g., StandardScaler) to model inputs
   - Note: Scaling was *not applied* for Decision Trees in one comparison

> ⚠️ The only algorithm tested without scaling was **Decision Trees**, and it gave a result almost identical to the scaled version — a common behavior for tree-based models.

---

## 📊 Model Results — Precision Scores

| Algorithme       | Precision |
|------------------|-----------|
| Decision Trees   | 0.658537  |
| SVC              | 0.779297  |
| XGBoost          | 0.764228  |
| KNN              | 0.780876  |

---

## 📌 Interpretation

- **KNN (0.7809)** and **SVC (0.7793)** performed best in terms of precision.  
  ➤ Both are sensitive to feature scaling, which improved their results significantly.

- **XGBoost (0.7642)** also showed strong performance.  
  ➤ As a tree-based ensemble, it’s less dependent on scaling but still effective.

- **Decision Trees (0.6585)** showed lower precision.  
  ➤ Because the model is based on splits rather than geometric distances, scaling has minimal effect.

**Conclusion:**  
Feature scaling is essential for distance- and margin-based algorithms (KNN, SVC), while tree-based models (Decision Trees, XGBoost) are less sensitive to it. The best-performing models here were KNN and SVC.

---

## 🛠️ How to Run This Project

### 1. Clone the Repository
```bash
git clone https://github.com/Abderaouf-KHELFAOUI/spam-classification.git
cd spam-classification
