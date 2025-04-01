# 🌾 Predicting Relevance of Classified Farm Ads (FarmAds Project)

## 🧠 Project Objective

Classified ad platforms serving farming communities often face issues with **spam**, **irrelevant posts**, or **automated content**. This project builds **machine learning models** to automatically classify ads as either **relevant (1)** or **not relevant (-1)**.

---

## 🧾 Dataset Details

- File: `FarmAds.csv`
- 4,143 ads (text + label)
- Variables:
  - `text`: Ad content
  - `label`: Relevance flag (1 = relevant, -1 = not relevant)
  - `doc_id`: Unique identifier

---

## 🔍 Workflow Summary

### 1️⃣ Preprocessing:
- Convert text to lowercase
- Remove punctuation & stop words
- Apply stemming
- Convert to **Document-Term Matrix (DTM)**
- Remove sparse terms (threshold: 94%)

### 2️⃣ Modeling Techniques

| Model           | Accuracy | Sensitivity | Specificity | Kappa  |
|----------------|----------|-------------|-------------|--------|
| Naive Bayes     | 72.87%   | 93.61%      | 54.75%      | 0.47   |
| SVM (Linear)    | 89.05%   | 93.78%      | 84.92%      | 0.78   |
| SVM (RBF Kernel)| 88.33%   | 87.05%      | 89.44%      | 0.76   |

> 📌 SVM (Linear) delivered the best overall classification accuracy and generalizability.

---

## 📊 Visuals (Optional)

- Word cloud of top terms
- DTM sparsity summary
- Confusion matrices for each model

---

## 🧪 Libraries Used

- `tm`, `SnowballC` – for text mining
- `klaR` – Naive Bayes
- `kernlab` – SVM modeling
- `caret` – Splitting, modeling, evaluation



