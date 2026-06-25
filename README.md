# 🌾 Smart Farming Through Multi-Temporal Climate Based AI for Agricultural Decision Support

> **B.Tech Final Year Project | CSE Department | AITAM, Andhra Pradesh | April 2026**

> 🏆 **Research Paper accepted for Oral Presentation at WAMS 2026 International Conference (IEEE) — Paper ID: 483**

---

## 👩‍💻 Team Members

| Name | Roll Number |
|---|---|
| Kolli Chaithra Jyotshna | 22A51A0594 |
| Behara Revathi Kusuma | 22A51A0572 |
| Kondeti Akhil Lokesh | 22A51A0596 |
| Kondaka Tarun Sai | 23A55A0514 |
| Valurouthu Uday Chandra Naidu | 22A51A05D0 |

**Project Guide:** Dr. Y. Ramesh, M.Tech, Ph.D. — HOD, Dept of CSE, AITAM

---

## 📌 Project Overview

This project builds a **Smart Farming Decision Support System** using AI and multi-temporal climate data from NASA POWER (2015–2024). It analyses rainfall, temperature, soil moisture, and humidity to evaluate agricultural land suitability and give farmers practical recommendations — without needing expensive sensors or soil testing.

A custom index called **ACLI (Agricultural Condition Level Index)** is created to classify land into:
- 🔴 **Poor** — High climate stress, unfavorable for crops
- 🟡 **Moderate** — Average conditions
- 🟢 **Good** — Optimal conditions for farming

---

## 🎯 Problem Statement

Rural farmers cannot afford expensive soil testing labs or IoT sensor systems. This project provides a **free, scalable, AI-based alternative** using NASA climate datasets to help farmers make better decisions about irrigation, crop selection, and seasonal planning.

---

## 📁 Repository Structure & What Each File Does

```
📁 Smart-Farming-AI/
│
├── 📓 decision_tree_final.ipynb
│       → Loads NASA POWER Daily.csv dataset
│       → Handles missing values using mean imputation
│       → Creates monthly features (rainfall, temperature, humidity, soil moisture)
│       → Applies Min-Max normalization
│       → Computes Irrigation Index, Crop Index, and ACLI
│       → Trains Decision Tree Regressor & Classifier
│       → Evaluates using MAE, RMSE, R², Accuracy, F1-Score
│       → Plots Actual vs Predicted ACLI and Confusion Matrix
│       → Result: Accuracy = 90.48%
│
├── 📓 random_forest_final.ipynb
│       → Same preprocessing pipeline as Decision Tree
│       → Trains Random Forest Classifier (200 trees, max_depth=10)
│       → Used for model comparison experiments
│       → Evaluates accuracy and classification performance
│
├── 📓 gradient_boosting_final.ipynb
│       → Same preprocessing pipeline as Decision Tree
│       → Trains Gradient Boosting Regressor for ACLI, Irrigation & Crop Index
│       → Trains Gradient Boosting Classifier for land suitability
│       → Parameters: 200 estimators, learning rate = 0.05
│       → Evaluates and saves models using Joblib
│       → Plots Actual vs Predicted ACLI and Confusion Matrix
│       → Result: Accuracy = 92.61% ✅ (Best Model)
│
├── 📊 BATCH-21.pptx
│       → Full project presentation slides
│       → Covers problem statement, methodology, results & conclusion
│
└── 📄 Document_Batch_21_merged.pdf
        → Complete B.Tech project report
        → Includes literature survey, system design, source code & results
```

---

## 🧠 Technologies Used

| Category | Details |
|---|---|
| Language | Python 3.8+ |
| Platform | Google Colab / Jupyter Notebook |
| Dataset | NASA POWER Daily Climate Data (2015–2024) |
| ML Library | Scikit-learn |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Model Saving | Joblib |

---

## 🤖 Models & Results

### Model 1 — Decision Tree
- Baseline model
- Simple rule-based classification
- **Accuracy: 90.48%**

### Model 2 — Random Forest
- Ensemble of 200 decision trees
- Used for comparison experiments

### Model 3 — Gradient Boosting ✅ Final Model
- Iteratively corrects errors of previous trees
- **Accuracy: 92.61%** — Best performance

---

## 📊 Performance Results

### Regression (Predicting ACLI values)
| Model | MAE | RMSE | R² Score |
|---|---|---|---|
| Decision Tree | 0.0250 | 0.0414 | 0.9622 |
| **Gradient Boosting** | **0.0165** | **0.0238** | **0.9875** |

### Classification (Land Suitability)
| Model | Accuracy | Precision | Recall | F1-Score |
|---|---|---|---|---|
| Decision Tree | 90.48% | 0.91 | 0.90 | 0.91 |
| **Gradient Boosting** | **92.61%** | **0.93** | **0.93** | **0.93** |

---

## 🔄 How the Code Works (Step by Step)

```
Step 1 → Load NASA POWER Daily.csv from Google Drive
Step 2 → Create Date index from YEAR + DOY columns
Step 3 → Replace -999 values with NaN
Step 4 → Fill missing values using column mean
Step 5 → Create 30-day rolling monthly features
         (cumulative rainfall, avg temperature, avg humidity, avg soil moisture)
Step 6 → Normalize all features using Min-Max Scaling
Step 7 → Compute agricultural indices:
         Irrigation Index = (soil moisture + rainfall) / 2
         Crop Index = (temperature + humidity + soil moisture) / 3
         ACLI = (rainfall + temperature + humidity + soil moisture) / 4
Step 8 → Label land as Low / Medium / High based on ACLI thresholds
Step 9 → Split data 80% train / 20% test (no shuffle — preserves time order)
Step 10 → Train and evaluate ML models
Step 11 → Generate farming recommendations
```

---

## 🌟 Key Achievements

- ✅ Introduced **ACLI** — a novel climate-based land suitability index
- ✅ **92.61% accuracy** with Gradient Boosting
- ✅ Uses **free NASA POWER data** — zero hardware cost
- ✅ Actionable output: irrigation scheduling, crop selection, seasonal planning
- ✅ Scalable for rural and resource-limited farming regions
- ✅ **IEEE WAMS 2026 accepted paper** 🏆

---

## 🌍 Key Findings

- 🌧️ **Monsoon season** → Land classified as **Good** (sufficient rainfall)
- ☀️ **Summer season** → Land classified as **Poor** (high climate stress)
- 🍂 **Transitional seasons** → Land classified as **Moderate**

---

## 🏛️ Institution

**Aditya Institute of Technology and Management (AITAM)**
Dept. of Computer Science & Engineering
K.Kotturu, Tekkali, Srikakulam — 532201, Andhra Pradesh
*Accredited by NBA & NAAC with A+ | Affiliated to JNTUGV*

---

© 2026 Team Batch 21 — AITAM CSE. All rights reserved.
