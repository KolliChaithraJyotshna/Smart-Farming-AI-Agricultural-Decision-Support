# 🌾 Smart Farming Through Multi-Temporal Climate Based AI for Agricultural Decision Support

> **B.Tech Final Year Project | CSE Department | AITAM, Andhra Pradesh | April 2026**
> 
> 🏆 **Research paper accepted for Oral Presentation at WAMS 2026 International Conference (IEEE) — Paper ID: 483**

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

This project develops an intelligent **Smart Farming Decision Support System** using Artificial Intelligence and multi-temporal climate data. It analyzes key agricultural parameters such as **rainfall, temperature, soil moisture, and humidity** from NASA POWER datasets to evaluate land suitability and provide data-driven farming recommendations.

A novel **Agricultural Condition Level Index (ACLI)** is introduced to classify agricultural land into:
- 🔴 **Poor** — Unfavorable conditions
- 🟡 **Moderate** — Average conditions
- 🟢 **Good** — Optimal conditions for cultivation

---

## 🎯 Problem Statement

Traditional farming relies on expensive soil testing and IoT sensors that are not accessible to rural farmers. This system provides a **cost-effective, scalable alternative** using freely available NASA climate datasets — no expensive hardware required.

---

## 🧠 Domain & Technologies

| Category | Details |
|---|---|
| Domain | Artificial Intelligence & Machine Learning |
| Sub-domain | Agricultural Data Analytics |
| Dataset | NASA POWER (2015–2024) |
| Language | Python 3.8+ |
| Environment | Jupyter Notebook / Google Colab |
| ML Framework | Scikit-learn |
| Key Libraries | Pandas, NumPy, Matplotlib, Seaborn, Joblib |

---

## 🤖 Machine Learning Models

### Model 1 — Decision Tree (Baseline)
- Rule-based classification using entropy and information gain
- Accuracy: **90.48%**
- Interpretable and easy to understand

### Model 2 — Gradient Boosting (Final Model ✅)
- Ensemble learning — each tree learns from previous errors
- Accuracy: **92.61%**
- Better generalization and higher precision across all classes

---

## 📊 Model Performance Results

### Regression Performance
| Model | Index | MAE | RMSE | R² Score |
|---|---|---|---|---|
| Decision Tree | Irrigation Index | 0.0244 | 0.0350 | 0.9824 |
| Decision Tree | Crop Index | 0.0290 | 0.0483 | 0.9435 |
| Decision Tree | ACLI | 0.0250 | 0.0414 | 0.9622 |
| **Gradient Boosting** | **Irrigation Index** | **0.0107** | **0.0152** | **0.9967** |
| **Gradient Boosting** | **Crop Index** | **0.0166** | **0.0238** | **0.9863** |
| **Gradient Boosting** | **ACLI** | **0.0165** | **0.0238** | **0.9875** |

### Classification Performance
| Model | Accuracy | Precision | Recall | F1-Score |
|---|---|---|---|---|
| Decision Tree Classifier | 90.48% | 0.91 | 0.90 | 0.91 |
| **Gradient Boosting Classifier** | **92.61%** | **0.93** | **0.93** | **0.93** |

---

## 🔄 System Workflow

```
NASA POWER Climate Data (2015–2024)
        ↓
Data Preprocessing
(Missing Value Handling + Min-Max Normalization + Temporal Aggregation)
        ↓
Feature Engineering
(Irrigation Index + Crop Index + ACLI Computation)
        ↓
Train-Test Split (80/20 — No Shuffle to preserve temporal order)
        ↓
ML Model Training
(Decision Tree  ←→  Gradient Boosting)
        ↓
Model Evaluation
(Accuracy, Precision, Recall, F1-Score, RMSE, MAE, R²)
        ↓
Agricultural Decision Support Output
(Irrigation Scheduling + Crop Suitability + Seasonal Recommendations)
```

---

## 📁 Repository Structure

```
📁 Smart-Farming-AI/
├── 📓 decision_tree_final.ipynb          # Decision Tree model implementation
├── 📓 random_forest_final.ipynb          # Random Forest experiments
├── 📓 gradient_boosting_final.ipynb      # Gradient Boosting model (Final)
├── 📊 BATCH-21.pptx                      # Project presentation slides
└── 📄 Document_Batch_21_merged.pdf       # Complete project report
```

---

## 🌟 Key Contributions

- ✅ Introduced **ACLI (Agricultural Condition Level Index)** — a novel composite climate metric
- ✅ Achieved **92.61% accuracy** with Gradient Boosting on land suitability classification
- ✅ Used **freely available NASA POWER data** — no expensive sensors or IoT required
- ✅ Provides actionable recommendations for **irrigation, crop selection & seasonal planning**
- ✅ **Cost-effective & scalable** — suitable for rural and resource-constrained regions
- ✅ Research paper **accepted at WAMS 2026 IEEE International Conference**

---

## 🌍 Key Findings

- 🌧️ **Monsoon season** → Land classified as **Good** (High ACLI due to rainfall)
- ☀️ **Summer season** → Land classified as **Poor** (High climate stress)
- 🍂 **Transitional seasons** → Land classified as **Moderate**

---

## 🔮 Future Scope

- Integration of satellite imagery (NDVI) for in-season crop monitoring
- Real-time deployment using NASA POWER API
- Explainable AI (SHAP) for transparent predictions
- Expansion to multiple geographic regions across India
- Incorporation of market pricing and crop calendar data

---

## 🏆 Achievement

> 📜 Research paper titled **"Smart Farming through Multi Temporal Climate based AI for Agricultural Decision Support"** accepted for **Oral Presentation at WAMS 2026 International Conference (IEEE)** — Paper ID: 483

---

## 🏛️ Institution

**Aditya Institute of Technology and Management (AITAM)**
Department of Computer Science and Engineering
K.Kotturu, Tekkali, Srikakulam — 532201, Andhra Pradesh
*Accredited by NBA & NAAC with A+ | Affiliated to JNTUGV*

---

## 📄 License

This project was developed as a Final Year B.Tech project.
All rights reserved © 2026 — Team Batch 21, AITAM CSE
