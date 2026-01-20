# Optimizing Healthcare Resource Allocation for Diabetic Patients in Kenya Using Machine Learning

![Diabetes Healthcare Banner](images/diabetes_banner.jpg)

---

## 1. Business Understanding

### Problem Statement
Diabetes-related hospital readmissions place significant pressure on Kenya’s already constrained healthcare system. High readmission rates increase costs, reduce hospital capacity, and often indicate gaps in discharge planning and follow-up care.

### Project Objective
To build a machine learning model that predicts **30-day hospital readmission risk** for diabetic patients, enabling:
- Targeted post-discharge interventions
- Efficient allocation of limited healthcare resources
- Improved patient outcomes

### Business Success Criteria (Kenya Context)
- **Recall ≥ 65%** (priority metric to avoid missing high-risk patients)
- Actionable insights that inform discharge planning and policy decisions

---

## 2. Data Understanding

### Dataset Overview
- **Source:** Hospital admission records (101,766 encounters)
- **Target Variable:** Readmission within 30 days (binary)
- **Features:** Demographics, diagnoses, medications, hospital utilization

### Key Data Challenges
- Severe class imbalance (~11% readmitted)
- High missingness in selected features (e.g. weight)
- Encoded categorical variables requiring mapping for interpretability

---

## 3. Exploratory Data Analysis (EDA)

EDA was conducted to understand patterns and risk factors associated with readmission.

### Key Visual Insights
- Distribution of 30-day readmissions
- Readmission rates by diagnosis group
- Relationship between length of stay and readmission
- Correlation between hospital utilization features and readmission

#### Example EDA Visuals
![Readmission by Diagnosis](images/readmission_by_diagnosis.png)
![Readmission by Time in Hospital](images/readmission_by_time.png)

### Key Findings
- Higher hospital utilization strongly correlates with readmission
- Certain discharge dispositions show significantly higher risk
- Longer hospital stays are associated with increased readmission probability

---

## 4. Data Preparation & Feature Engineering

### Preparation Steps
- Binary target creation for 30-day readmission
- Removal of features with excessive missing values
- Encoding categorical variables
- Stratified train-test split

### Feature Engineering
- Hospital utilization metrics (total visits, emergency visits)
- Grouped diagnosis categories
- Medication change indicators
- Simplified age groupings

These steps improved model performance and clinical interpretability.

---

## 5. Modeling

Three models were trained and evaluated:
1. **Logistic Regression** (baseline and improved with SMOTE)
2. **Random Forest**
3. **XGBoost**

### Modeling Focus
- Handling class imbalance
- Threshold optimization to prioritize Recall
- Hyperparameter tuning

---

## 6. Model Evaluation

Models were evaluated using metrics aligned with the business objective.

### Model Performance Summary

| Model | Recall | Precision | AUC |
|-----|-------|----------|-----|
| Logistic Regression | 0.651 | 0.131 | 0.588 |
| Random Forest | **0.690** | 0.154 | 0.660 |
| XGBoost | 0.655 | **0.163** | **0.672** |

### Evaluation Visuals
![Model Comparison](images/model_comparison.png)
![Random Forest Confusion Matrix](images/random_forest_cm.png)

---

## 7. Conclusion

Machine learning can effectively identify diabetic patients at high risk of readmission in a resource-constrained healthcare setting.  
Among the models tested, **Random Forest** achieved the best balance between predictive performance and practical deployment needs.

---

## 8. Recommendations

### Final Model Recommendation
✅ **Random Forest Classifier**

### Why Random Forest?
- Highest Recall (69%) — meets Kenya healthcare priority
- Fewer false alarms than Logistic Regression
- Clear feature importance for policy and clinical decisions

### Business & Policy Recommendations
- Prioritize high-risk patients for enhanced discharge planning
- Use predictions to guide follow-up care allocation
- Integrate model insights into hospital decision-support systems

---

## Tools & Technologies
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib / Seaborn
- Jupyter Notebook

---
 

@MoringaCapstoneProject_Group4



