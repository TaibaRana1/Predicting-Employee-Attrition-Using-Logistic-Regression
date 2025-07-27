## Predicting-Employee-Attrition-Using-Logistic-Regression
Employee turnover is a major challenge impacting productivity and performance. This project uses logistic regression to predict which employees are likely to leave, helping HR teams take proactive steps to reduce attrition.

📌 Objectives
Identify Key Drivers: Analyze features like age, income, job role, and overtime that impact attrition.
Feature Engineering: Create new features (e.g., loyalty_ratio, promotion_delay_ratio) to better reflect employee behavior.
Model Development: Train and fine-tune a logistic regression model using Grid Search.
Evaluation: Assess model using accuracy, precision, recall, F1-score, and a confusion matrix.
Actionable Insights: Provide data-driven suggestions to help reduce employee churn.

## ⚙️ Data Preprocessing
+  No missing values detected, but checks were performed.
 +    One-Hot Encoding applied to categorical columns.
  +   Outliers handled using the IQR method.
+     Dropped constant or irrelevant columns: EmployeeCount, EmployeeNumber, Over18, StandardHours.

## 📊 Exploratory Data Analysis (EDA)
   High Attrition Rate: Most employees have left (1200+), vs ~250 who stayed.
   By Age: Peak attrition between ages 28–32.
   By Income: Higher attrition in employees earning ₹2000–₹3000. Lower in high-income groups.
   By Gender: Male attrition ≈ 1.7x female attrition.

## 🧪 Feature Engineering
loyalty_ratio = YearsAtCompany / (TotalWorkingYears + 1)
promotion_delay_ratio = YearsSinceLastPromotion / (YearsAtCompany + 1) (capped at 5)
normalized_income = MonthlyIncome / (JobLevel + 1) (capped at 20,000)

## 📈 Model Performance
Accuracy: 71.4%
Precision / Recall / F1 (Class 1 - Attrition):
Precision: 0.27
Recall: 0.67
F1-Score: 0.38
Confusion Matrix:
TN: 184, FP: 71, FN: 13, TP: 26

➡️ The model performs well for majority class (non-leavers), but struggles with precision for minority class (leavers), likely due to class imbalance.

## Tools Used
Python, Pandas, Seaborn, Plotly, Scikit-learn
