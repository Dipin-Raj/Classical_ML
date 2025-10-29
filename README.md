# 🧠 OMNIe Solutions – AI/ML Internship Evaluation Projects

**Name:** Dipin Raj  
**University:** Chandigarh University  
**Phone:** +91 6235876977  
**Email:** dipinr505@gmail.com  
**Location:** Wayanad, Kerala, India  
**Company:** Omnie Solutions Pvt. Ltd., Noida  
**Mentors:** Mr. Chhatra Pratap & Mr. Anand Shukla  
**Assignment:** Evaluation 01 | **Job Role:** AI/ML Intern  

---

## 📂 Repository Structure
```
│── Notebook/ # Contains Google Colab notebooks for each task
│ ├── OMNIe_Task_1.ipynb
│ ├── OMNIe_Task_2.ipynb
│
│── Graphs/ # All EDA visualizations, ROC curves, correlation plots
│
│── Report & Documentation/ # Project reports and supporting documents
│ ├── OMNIe Solutions_Predicting Operational Efficiency of Manufacturing Teams.pdf
│ ├── OMNIe Solutions_Retail Web Session Intelligence.pdf
│
│── README.md # Project overview (this file)
```

## 🧩 TASK 1: Predicting Team Efficiency in a Manufacturing Unit

### 📘 Dataset
This dataset records the **daily operational statistics** of production teams in a garment manufacturing plant.  
Each record represents a single day’s performance of a team, including:
- **Production Features:** `plannedEfficiency`, `standardMinuteValue`, `workInProgress`, `performanceBonus`
- **Workforce Features:** `idleMinutes`, `workerCount`, `idleWorkers`
- **Contextual Features:** `dayOfWeek`, `productionDept`, etc.  
- **Target Variable:** `efficiencyScore`

### 🎯 Objective
To build a **regression model** that predicts team efficiency based on production and workforce-related variables, identifying the most influential factors behind daily operational performance.

### ⚙️ Methodology
- Data Cleaning & Missing Value Treatment  
- Outlier Mitigation using **range-based thresholds from scatter plots**  
- Department-wise Segmentation (Stitching vs Finishing & Quality)  
- Feature Scaling and One-Hot Encoding  
- Model Training using:
  - Linear Regression (Scratch + Sklearn)
  - Decision Tree Regressor
  - Random Forest Regressor

### 📊 Results
| Model | R² Score | MSE |
|-------|-----------|-----|
| Linear Regression (Scratch) | 0.808 | 0.00388 |
| Decision Tree Regressor | 0.741 | 0.00422 |
| Random Forest Regressor | **0.856** | **0.00234** |

**Insight:**  
The **Random Forest Regressor** achieved the best performance, showing that **planned efficiency** and **performance bonus** were key drivers of productivity.

---

## 💡 TASK 2: Retail Web Session Intelligence (RWSI)

### 📘 Dataset
The **Retail Web Session Intelligence (RWSI)** dataset simulates **user browsing sessions** on a digital retail platform selling consumer and lifestyle products.  
Each record represents an **anonymized session**, capturing:
- **Behavioral Metrics:** `pageEngagementScore`, `visitDuration`, `clickRate`
- **Contextual Attributes:** `visitMonth`, `userCategory`, `region`, etc.
- **Target Variable:** `MonetaryConversion` (Yes/No)

### 🎯 Objective
To develop a **classification model** that predicts the **likelihood of conversion** (purchase intent) based on user engagement, browsing behavior, and contextual factors.

### ⚙️ Methodology
- Outlier Detection via Scatter Plots & Range Inference  
- **Semi-Synthetic Balancing**: Created diverse “Yes” samples using feature-specific ranges + controlled randomness  
- One-Hot Encoding for Categorical Features  
- Feature Scaling and Normalization  
- Model Training using:
  - Logistic Regression (Standard & Scaled)
  - Decision Tree
  - Random Forest
  - XGBoost

### 📈 Results
| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|--------|-----------|------------|---------|-----------|----------|
| XGBoost | 0.865 | 0.87 | 0.86 | 0.86 | 0.94 |
| Random Forest | **0.867** | 0.87 | 0.87 | 0.87 | **0.94** |
| Decision Tree | 0.865 | 0.87 | 0.87 | 0.87 | 0.94 |
| Logistic Regression (Scratch) | 0.810 | 0.81 | 0.81 | 0.81 | 0.90 |

**Insight:**  
Random Forest and XGBoost provided **balanced precision-recall tradeoffs** and **smooth convergence**, validating the effectiveness of the new **range-based oversampling** and **outlier refinement** strategies.

---

## 🧠 Key Learnings
- Importance of **domain-specific preprocessing** in both industrial and retail datasets.  
- Semi-synthetic balancing using **controlled randomness** preserved data authenticity.  
- Ensemble models like **Random Forest** generalized better under class imbalance.  
- Feature importance analysis linked **engagement metrics** (Task 2) and **planning metrics** (Task 1) to real-world outcomes.

---

## ⚙️ Environment & Tools
- **Platform:** Google Colab  
- **Language:** Python 3.12  
- **Libraries:** pandas, numpy, scikit-learn, xgboost, matplotlib, seaborn, plotly  
- **Visualization:** Correlation Maps, ROC Curves, Scatter Plots, Heatmaps  
- **Version Control:** GitHub

---

## 📜 Acknowledgements
Special thanks to **Omnie Solutions Pvt. Ltd.**, **Mr. Chhatra Pratap**, and **Mr. Anand Shukla** for mentorship and guidance throughout the project.

---

### 📎 Reference
📂 Full reports and detailed documentation are available in the [`Documentation/`](./Documentation) folder.  
🧾 All source notebooks are available in the [`Notebook/`](./Notebook) directory.
📊 Visual results and graphs can be found in [`Graphical Representations/`](./Graphical%20Representations).

⭐ **Author:** [Dipin Raj](https://www.linkedin.com/in/dipin-raj-539788231/)
