# git_practice3
# 🇰🇪 Predicting Diabetes Readmission in Kenya Using Machine Learning

![Diabetes Healthcare Banner](images/diabetes_banner.jpg)

## 📌 Project Summary

Diabetes-related hospital readmissions place a heavy burden on Kenya’s healthcare system, increasing costs, overcrowding facilities, and signaling gaps in patient follow-up care.  

This project applies **machine learning** to predict whether a diabetic patient is likely to be **readmitted after discharge**, enabling hospitals to take early preventive action.

The analysis strictly follows the **CRISP-DM (Cross-Industry Standard Process for Data Mining)** framework to ensure clarity, reproducibility, and strong business alignment.

---

## 🧭 CRISP-DM PHASES

---

## **Phase 1: Business Understanding**

### 🔹 Business Problem
Hospital readmissions:
- Increase operational costs
- Reduce hospital efficiency
- Often indicate insufficient discharge planning or patient monitoring

### 🔹 Business Objective
To build a predictive model that:
- Identifies diabetic patients at high risk of readmission
- Supports hospitals in making data-driven discharge and follow-up decisions

### 🔹 Success Criteria
- A machine learning model with reliable predictive performance
- Clear insights that can guide healthcare decision-making
- Actionable recommendations for reducing readmission rates

---

## **Phase 2: Data Understanding**

### 📂 Dataset Description
- Patient hospital admission records
- Combination of demographic, clinical, and treatment features
- Target variable: **Readmission status**

### 🔹 Key Variables
- Patient age and gender
- Admission type
- Medical history
- Treatment and medication information

### 🔹 Initial Observations
- Presence of missing values
- High number of categorical variables
- Class imbalance in readmission outcomes

---

## **Phase 3: Exploratory Data Analysis (EDA)**

EDA was conducted to understand patterns, relationships, and potential predictors of readmission.

### 📊 Distribution of Readmission Status
![Readmission Distribution](images/readmission_distribution.png)

### 📊 Age Distribution of Patients
![Age Distribution](images/age_distribution.png)

### 📊 Gender vs Readmission
![Gender vs Readmission](images/gender_readmission.png)

### 📊 Feature Correlation Heatmap
![Correlation Heatmap](images/correlation_heatmap.png)

### 🔍 Key Insights from EDA
- Readmission is not evenly distributed across patients
- Certain age groups show higher readmission rates
- Some features demonstrate meaningful correlations with readmission

---

## **Phase 4: Data Preparation**

This phase focused on transforming raw data into a machine-learning-ready format.

### 🧹 Preprocessing Steps
- Handling missing values
- Encoding categorical variables
- Feature scaling
- Addressing class imbalance
- Splitting data into training and testing sets

### 🔹 Rationale
Proper preprocessing improves:
- Model accuracy
- Generalization
- Interpretability of results

---

## **Phase 5: Modeling**

Multiple models were trained to compare performance and robustness.

### 🤖 Models Implemented
1. **Logistic Regression**
   - Baseline model
   - Easy to interpret
2. **Decision Tree Classifier**
   - Captures non-linear relationships
3. **Random Forest Classifier**
   - Ensemble model
   - Handles feature interactions effectively

---

## **Phase 6: Model Evaluation**

Models were evaluated using:
- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrices

### 🔹 Logistic Regression Confusion Matrix
![Logistic Regression CM](images/logistic_regression_cm.png)

### 🔹 Decision Tree Confusion Matrix
![Decision Tree CM](images/decision_tree_cm.png)

### 🔹 Random Forest Confusion Matrix
![Random Forest CM](images/random_forest_cm.png)

### 📈 Model Performance Comparison
![Model Comparison](images/model_comparison.png)

---

## **Phase 7: Results & Interpretation**

### 🏆 Best Performing Model
**Random Forest Classifier**

#### Reasons:
- Higher predictive accuracy
- Better balance between recall and precision
- Strong handling of complex feature relationships

---

## **Phase 8: Conclusions**

- Machine learning can effectively predict diabetes readmission risk
- Proper preprocessing and class balancing significantly impact performance
- Ensemble models outperform simpler models in this task

---

## **Phase 9: Recommendations**

### 🏥 For Healthcare Providers
- Integrate the model into discharge planning systems
- Flag high-risk patients for follow-up care
- Allocate resources more efficiently

### 🔄 For Future Improvements
- Incorporate real-time patient monitoring data
- Use larger, more localized Kenyan healthcare datasets
- Explore advanced models such as Gradient Boosting

---

## 🛠 Tools & Technologies

- **Python**
- Pandas & NumPy
- Matplotlib & Seaborn
- Scikit-learn
- Jupyter Notebook

---

## 📁 Project Structure


