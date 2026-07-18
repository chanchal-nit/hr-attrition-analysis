# hr-attrition-analysis
# 👔 IBM HR Analytics — Employee Attrition Prediction

A consulting-style ML project predicting which employees are likely 
to leave the company using IBM's HR dataset of 1,470 employees.

## Business Problem
Employee attrition costs companies 6-9 months of an employee's salary 
in recruitment and training. Can we predict who will leave before they do?

## Dataset
- 1,470 employees, 35 features
- Target: Attrition (Yes/No) — 84% stayed, 16% left (imbalanced!)
- Source: IBM HR Analytics Dataset (Kaggle)

## What I Did
1. EDA — explored 10+ factors affecting attrition
2. Feature engineering — encoded 4 categorical columns
3. Dropped useless columns (all-same-value features)
4. Compared 4 ML models on imbalanced data
5. Applied class balancing to improve minority class detection
6. Feature importance analysis — identified top attrition drivers

## Key Findings
- **Singles** leave more than married employees
- **Early 30s, Job Level 1** employees have highest attrition
- **Low income + overtime** = strongest combination for leaving
- **R&D and Sales** departments have most attrition
- **Distance from home** is a surprisingly strong predictor

## Model Results

| Model | Accuracy | AUC | Recall (Leavers) |
|-------|----------|-----|------------------|
| KNN | 88.78% | 0.594 | 0.15 ❌ |
| Decision Tree | 85.37% | 0.611 | Low |
| Random Forest | 87.07% | 0.717 | Low |
| Logistic Regression | 87.76% | 0.760 | 0.31 |
| **Balanced LR** | **74%** | **0.760** | **0.69 🏆** |

## Key ML Lesson
Accuracy is misleading on imbalanced data! KNN got 88.78% accuracy 
but only caught 15% of actual leavers — completely useless for business.
Balanced Logistic Regression caught 69% of leavers — the real winner!

## Business Recommendations
- **Work from home** for employees living 30+ km away
- **Overtime bonuses** — compensate extra work fairly  
- **Salary benchmarking** — pay competitively or lose talent
- **Growth paths** for Job Level 1 — lack of growth = resignation
- **Focus retention** on R&D and Sales departments

## Tools Used
Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn

## Final Conclusion
> Employee attrition is predictable and preventable. Compensation, 
> work-life balance, and career growth are the three pillars of 
> employee retention. Fix these → reduce attrition significantly.

## IE Connection
This analysis is directly applicable to manufacturing and supply chain — 
high attrition in warehouse and logistics roles costs companies millions 
annually. Same ML approach applies to factory floor retention! 🏭
