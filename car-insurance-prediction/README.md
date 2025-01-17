# Car Insurance Claim Prediction

This project focuses on developing a predictive model to assess the probability of car insurance claims. The objective is to understand the factors influencing claim frequency and severity over six months, enabling insurance companies to better assess risk and determine appropriate premiums for policyholders.

## Problem Statement
The goal is to predict whether a car insurance policyholder will file a claim (`is_claim`: 1) or not (`is_claim`: 0) within six months. The dataset contains imbalanced classes, with significantly more `no-claim` cases than `claim` cases.

## Dataset
The dataset includes various features related to policyholders, vehicles, and demographics. Key features include:
- **policy_tenure**: Duration of the policy in months
- **age_of_policyholder**: Age of the policyholder
- **age_of_car**: Age of the car in years
- **population_density**: Population density of the policyholder's area
- **area_cluster**: Categorical representation of geographic regions

### Target Variable
- `is_claim`: Binary variable where 1 indicates a claim was filed, and 0 indicates no claim.

## Steps Followed in the Project

1. **Data Preprocessing:**
   - Handled missing values and encoded categorical variables.
   - Scaled numerical features using StandardScaler.

2. **Class Imbalance Handling:**
   - Used SMOTE (Synthetic Minority Oversampling Technique) to balance the dataset.

3. **Exploratory Data Analysis (EDA):**
   - Analyzed correlations between features and the target variable.
   - Identified relevant patterns such as the relationship between `policy_tenure` and claims.

4. **Feature Selection:**
   - Selected key features based on domain knowledge and statistical importance.

5. **Model Selection and Training:**
   - Tried various models, including:
     - Logistic Regression
     - Random Forest Classifier
     - XGBoost
   - Performed hyperparameter tuning using RandomizedSearchCV to optimize model performance.

6. **Evaluation Metrics:**
   - Used precision, recall, F1-score, and accuracy to evaluate models.
   - Focused on achieving higher recall for the minority class (claims).

## Final Models Selected

1. **Random Forest Classifier with Hyperparameter Tuning:**
   - Achieved a balance between precision and recall for both classes.
   - Performance Metrics:
     - Precision (Class 1): 0.10
     - Recall (Class 1): 0.35
     - F1-Score (Class 1): 0.15

2. **XGBoost Classifier with Hyperparameter Tuning:**
   - Delivered competitive results with high precision for non-claims and acceptable recall for claims.
   - Performance Metrics:
     - Precision (Class 1): 0.09
     - Recall (Class 1): 0.02
     - F1-Score (Class 1): 0.03

## Key Insights
- **Class Imbalance:** SMOTE improved recall for the minority class but introduced challenges in overall model performance.
- **Feature Importance:** Variables like `policy_tenure` and `age_of_car` had significant impacts on predictions.
- **Threshold Tuning:** Adjusting decision thresholds helped improve recall for claims.

## Challenges Faced
- Class imbalance leading to biased predictions.
- Difficulty in achieving a high F1-score for the minority class.

## Tools and Technologies Used
- **Programming Language:** Python
- **Libraries:** pandas, numpy, scikit-learn, imbalanced-learn, LightGBM, XGBoost, matplotlib, seaborn
- **Model Tuning:** RandomizedSearchCV

## How to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/chaitali1492/machine-learning-module.git
   ```
2. Run the Jupyter Notebook:
   ```bash
   jupyter notebook car-insurance-prediction/Car_Insurance_Pred.ipynb
   ```
## Conclusion
This project provides a comprehensive framework for predicting car insurance claims, balancing business needs and technical challenges. The insights gained can help insurers design more effective risk assessment strategies.

## License
This project is licensed under the [MIT License](LICENSE).

