# 🛍️ Retail Web Session Intelligence (RWSI) — Conversion Prediction

## 📌 Overview
This project focuses on analyzing and modeling **user behavior in digital retail sessions** to predict conversion events.  
Using the **Retail Web Session Intelligence (RWSI)** dataset, we aim to uncover what drives successful purchase intent and differentiate **high-intent shoppers** from **casual browsers** through data-driven insights.

---

## 🧠 Objective
Develop a predictive model to estimate the likelihood of a **Monetary Conversion** based on user interaction patterns, engagement metrics, and contextual attributes.

---

## 🗂️ Repository Structure
📦 RWSI-Classification
├── 📁 notebooks/ # Google Colab notebooks with full pipeline (EDA → Modeling → Evaluation)
├── 📁 graphical_reports/ # Visual insights, plots, and correlation maps
├── 📁 documentation/ # Methodology, results, and conclusion reports
├── 📄 README.md # Project overview (this file)
└── 📄 requirements.txt # Dependencies list

## ⚙️ Key Steps

### 1️⃣ Data Understanding
- Explored **session-level attributes** — including browsing time, engagement rate, traffic source, and session month.
- Identified behavioral differences between converting and non-converting sessions.

### 2️⃣ Preprocessing
- Removed null and inconsistent entries to improve reliability.  
- Introduced a **controlled semi-synthetic oversampling** technique using feature-specific scatter range inference and randomization to balance conversion classes.  
- Encoded categorical variables via **one-hot encoding** and applied **scaling** where necessary.

### 3️⃣ Modeling
Implemented and evaluated multiple classifiers:
- Logistic Regression (Standard & Scaled)
- Decision Tree
- Random Forest
- XGBoost

---

## 📊 Results
| Model | Accuracy | Precision (Class 1) | Recall (Class 1) | F1-Score (Class 1) |
|:------|:----------|:--------------------|:-----------------|:-------------------|
| XGBoost | 0.865 | 0.86 | 0.90 | 0.88 |
| Random Forest | **0.867** | **0.88** | **0.87** | **0.87** |
| Decision Tree | 0.865 | 0.87 | 0.87 | 0.87 |
| Logistic Regression | 0.814 | 0.84 | 0.78 | 0.81 |

**Best Performer:** Random Forest  
Demonstrated the most stable trade-off between recall and precision, showing strong adaptability to both classes.

---

## 🧩 Key Insights
- **Page Engagement Score** and **Visit Month** emerged as dominant predictors.
- The **semi-synthetic balancing** improved minority class recognition without biasing the dataset.
- Slow ROC convergence indicates potential hidden behavioral dependencies worth further exploration.

---

## 📘 Documentation
- Detailed **Methodology**, **Results**, and **Conclusion** can be found inside the `documentation/` folder.

---

## 🚀 Tools & Environment
- **Google Colab** (Python 3)
- **Libraries:** Pandas, NumPy, Matplotlib, Scikit-learn, XGBoost, Seaborn, Plotly

---

## 📈 Graphical Representations
All EDA and model evaluation visualizations (scatter plots, correlation heatmaps, ROC curves, and performance metrics) are stored under the `graphical_reports/` folder.

⭐ *If you found this project insightful, consider starring the repository!*
