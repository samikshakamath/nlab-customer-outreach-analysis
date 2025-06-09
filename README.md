# Optimizing Customer Outreach for N/LAB Platinum Deposit 

**Author:** Samiksha Kamath  
**Date of Original Creation:** December 25, 2024  
**Student ID:** 20703562

---

## 📊 Project Overview

This project analyzes and models customer response behavior to a financial product — the "N/LAB Platinum Deposit." Using a real-world styled dataset from N/LAB Enterprises, the goal is to improve telemarketing strategy through advanced data preprocessing, statistical analysis, and machine learning.

---

## 🧹 Data Preparation & Feature Engineering

- Removed columns with >50% missing or unknown values (e.g., `poutcome`)
- Dropped rows with missing target labels (`y`)
- Detected and removed outliers using IQR and z-score methods
- Engineered interaction features: `balance_duration_ratio`, `call_efficiency`
- Standard scaling applied to numerical features
- Removed non-informative or constant features

---

## 📈 Exploratory Data Analysis

- **Call Duration**: Most significant predictor of subscription success (correlation ~0.47)
- **Account Balance**: Higher balances → higher likelihood of subscription
- **Age**: Older individuals (especially >70) had higher conversion rates
- **Class Imbalance**: 88% "No", 12% "Yes" → tackled with evaluation focus on specificity and accuracy

---

## 🧠 Models and Evaluation

| Model              | Accuracy | Specificity | Precision |
|-------------------|----------|-------------|-----------|
| Logistic Regression | 83.52%   | 97.03%      | 69.09%    |
| Decision Tree       | 82.82%   | 95.80%      | 62.50%    |
| Random Forest       | 81.41%   | 94.58%      | 54.41%    |

- **Logistic Regression**: Best precision, strong for reducing unnecessary calls  
- **Random Forest**: Best for identifying more potential subscribers  
- **Decision Tree**: Clear interpretability, useful for strategy and targeting

---

## 📌 Key Business Recommendations

1. **Prioritize longer calls** – Duration strongly correlates with conversions  
2. **Optimize call efficiency** – Longer, more efficient calls are effective  
3. **Target age groups 30–50** – Best response rates  
4. **Focus on high-balance customers** – Greater interest in investment products  
5. **Use cellular contact** – Better engagement compared to other methods  
6. **Refine messaging scripts** – Based on age, balance, and call length  
7. **Deprioritize low-conversion groups** – e.g., unemployed, blue-collar roles  
8. **Tailor offers to financial status** – E.g., no housing loan = more receptive

---

## 🛠 Tools & Technologies

- **Python** – Data analysis, modeling (Pandas, NumPy, Matplotlib, Scikit-learn)
- **Jupyter Notebook** – Code execution and documentation
- **CSV Dataset** – Pre-cleaned and analyzed
- **PDF Report** – Final summary of findings and business insights

---

## 📂 Repository Contents

- `analysis.ipynb` – Full model and analysis code
- `cleaned_dataset.csv` – Processed dataset
- `report.pdf` – Final business analysis and recommendations

---

## 🚀 How to Use

1. Open the Jupyter notebook in Colab or VSCode
2. Upload `cleaned_dataset.csv`
3. Run cells to preprocess data, train models, and view results
4. Use output and report for business decision-making

