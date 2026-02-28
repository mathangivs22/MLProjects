# 🏥 Insurance Cost Factor Analysis

A statistical data analysis project to identify the key factors that significantly influence insurance charges, using a structured data pipeline involving EDA, preprocessing, feature engineering, and hypothesis testing.

---

## 📌 Problem Statement

What actually drives up your insurance cost? Is it your lifestyle, your location, or your demographics? This project uses statistical methods to answer that question with data — not guesswork.

---

## 📂 Dataset

- **Source:** Insurance dataset (CSV)
- **Features:** Age, Sex, BMI, Children, Smoker status, Region, Insurance Charges

---

## 🔬 Methodology

### 1. 🔍 Exploratory Data Analysis (EDA)
- Examined dataset shape, data types, and summary statistics
- Identified distributions and outliers across key variables
- Plotted graphs to visually understand feature distributions and relationships

### 2. 🧹 Data Cleaning & Preprocessing
- Handled missing values and duplicates
- Extracted numeric features for analysis
- Applied **Label Encoding** for binary categorical variables (e.g. smoker: yes/no)
- Applied **One-Hot Encoding** for multi-category variables (e.g. region)

### 3. 📊 Correlation Analysis
- Plotted a **Correlation Heatmap** to visualize relationships between numerical features
- Used **Pearson Correlation** to identify which numerical variables are linearly related to insurance charges

### 4. ⚙️ Feature Engineering & Scaling
- Created derived features such as **BMI categories** (e.g. Obese, Normal) for better categorical analysis
- Applied **Feature Scaling** to normalize numerical variables and remove bias

### 5. 📐 Chi-Square Test (Hypothesis Testing)
- Applied **Chi-Square Test** on categorical variables to statistically validate their association with insurance charges
- Null Hypothesis (H0): No association between the feature and insurance cost

---

## 📈 Key Findings

| Feature | Chi² Value | p-value | Decision |
|---|---|---|---|
| **Smoker** | 848.22 | 0.00000 | ✅ Reject H0 – Highly Significant |
| **Region (Southeast)** | 15.99 | 0.00113 | ✅ Reject H0 – Significant |
| **Gender (Female)** | 10.26 | 0.01649 | ✅ Reject H0 – Significant |
| **BMI Category (Obese)** | 8.52 | 0.03647 | ✅ Reject H0 – Significant |

### 💡 Insights
- **Smoking** is by far the most dominant factor (χ²=848), with a near-zero p-value — meaning there is virtually zero chance this relationship is a coincidence
- **Region, Gender and BMI** also play statistically significant roles, though considerably smaller in magnitude than smoking
- These findings can help insurance providers with **risk profiling and premium pricing strategies**

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python | Core programming language |
| Pandas | Data manipulation and cleaning |
| NumPy | Numerical computations |
| Matplotlib & Seaborn | Data visualization |
| SciPy | Chi-Square statistical testing |
| Google Colab | Development environment |

---

## 🚀 How to Run

1. Clone this repository
```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
```
2. Open the `.ipynb` file in [Google Colab](https://colab.research.google.com/) or Jupyter Notebook
3. Run all cells sequentially

---
