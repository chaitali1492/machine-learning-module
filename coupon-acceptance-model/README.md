# E-Commerce Coupon Acceptance Prediction  

## 📌 Project Overview  
This project predicts whether users will accept coupons based on driving scenarios and user attributes collected from an e-commerce platform. The objective is to optimize coupon distribution strategies and enhance user engagement.  

## 🎯 Problem Statement  
The dataset contains user behaviors, contextual attributes, and coupon details, influencing whether a user accepts a coupon. The challenge is accurately predicting coupon acceptance despite variations in user behavior, time, and location.  

## 📂 Dataset Information  
- **Total Records:** 12,684  
- **Target Variable:** `Accept (Y/N?)` (Binary: 1 = Accepted, 0 = Not Accepted)  
- **Features:** 25 (including user demographics, behavioral attributes, and contextual factors)  
- **Class Distribution:**  
  - ✅ **Accepted (1):** 56.5%  
  - ❌ **Not Accepted (0):** 43.4%  

## 🛠️ Data Preprocessing  
- **Handled Missing Values:** Imputed using mode  
- **Duplicate Records:** Removed 291 duplicates  
- **Outlier Detection:** No significant outliers found  
- **Feature Encoding:** Applied **Ordinal Encoding & One-Hot Encoding**  

## 📊 Exploratory Data Analysis  
- **Correlation Analysis:** No strong correlation with the target variable  
- **Class Distribution:** No major imbalance, so no resampling applied  

## 🤖 Model Selection & Evaluation  
| Model | Accuracy | Precision (Class 1) | Recall (Class 1) | F1-Score (Class 1) |  
|--------|----------|----------------|--------------|--------------|  
| Random Forest | 73% | 73% | 80% | 77% |  
| **Random Forest (Tuned)** | 74% | 74% | 80% | 77% |  
| **XGBoost (Final Model)** | **74%** | **75%** | **81%** | **78%** |  

### 🔥 Key Takeaways  
- **XGBoost performed best**, achieving an **81% recall and 75% precision**.  
- The model can help e-commerce platforms **improve targeted marketing strategies**.  

## 🚀 Deployment  
The trained model is available in this repository and can be integrated into an e-commerce system for real-time predictions.  

## How to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/chaitali1492/machine-learning-module.git
   ```
2. Run the Jupyter Notebook:
   ```bash
   jupyter notebook coupon-acceptance-model/E-commerce-checkpoint.ipynb
   ```

