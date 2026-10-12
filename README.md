# IBM-HR-ATTRITION
# 📌 Problem Statement
IBM is facing 16.12% annual attrition (237 out of 1470 employees). Replacing one employee costs ~1.5x salary. The goal is to predict attrition and identify key drivers.

## 📊 Dataset
- Source: IBM HR Analytics (Kaggle)
- Rows: 1470 Employees | Columns: 35 Features
- Target: Attrition (Yes/No) - Imbalanced (16% Yes)

## 🔍 Key Analysis & Insights (EDA)

*1. Who is leaving?*
- *Overtime is the #1 Killer:* Employees doing overtime have 30% attrition rate vs 10% without overtime.
- *Young & Single:* Age 18-30 and Single employees have highest attrition (~25%).
- *Low Satisfaction:* Job Satisfaction 1/4 has 3x more attrition.

*2. Department Wise:*
- Sales has highest attrition - 20.6%
- R&D - 13.8%
- HR - 19%

*3. Salary Factor:*
- Low Percent Salary Hike (11-13%) is strongly linked to attrition.

## 🤖 Model Building
I handled imbalance with class_weight='balanced'

| Model | Accuracy | Recall (Attrition) | F1-Score |
| :--- | :--- | :--- | :--- |
| Logistic Regression | 84% | 62% | 0.48 |
| *Random Forest (Final)* | *87%* | *78%* | *0.62* |

*Top 5 Reasons for Attrition (Feature Importance):*
1. OverTime
2. Job Satisfaction
3. Monthly Income
4. Age
5. Years At Company

## 💰 Business ROI - This is what matters to company
- Avg Replacement Cost per Employee: $15,000
- If our model helps retain just 50 employees/year:
- *Annual Saving = 50 * $15,000 = $750,000*

*My Recommendation to HR:*
1. Ban excessive overtime or give comp-off.
2. Focus on 1-on-1 for employees with Job Satisfaction <=2.
3. Salary hike review for employees with <13% hike.

## 🛠️ Tech Stack
Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Google Colab
