# Bank Customer Churn Prediction and Customer Lifetime Value (CLV) Optimization

## Project Overview
This project aims to tackle two key challenges in the banking industry:
1. **Customer Churn Prediction**: Identifying at-risk customers and understanding the factors driving churn.
2. **Customer Lifetime Value (CLV) Analysis**: Evaluating long-term customer profitability to prioritize retention efforts effectively.

**Author**: Hijir Della Wirasti  
**LinkedIn**: [Hijir Della Wirasti](https://www.linkedin.com/in/hijirdella/)  
**GitHub**: [Bank Customer Churn Prediction and CLV Optimization](https://github.com/hijirdella/Bank-Customer-Churn-Prediction-and-CLV-Optimization)

---

## Objectives
- Develop a machine learning model to predict customer churn with high accuracy and F1-score.
- Perform CLV segmentation to identify high-value customers and derive actionable insights.
- Provide practical recommendations to reduce churn and maximize customer lifetime value.

---

## Data Summary
The dataset includes customer demographics, financial behavior, product usage, and churn labels. The target variable (`Churn`) is highly imbalanced, requiring resampling techniques such as **SMOTE** (oversampling) and **RandomUnderSampler**.

---

## Tested Models
A total of 11 models were evaluated:
1. Logistic Regression  
2. Random Forest  
3. Gradient Boosting  
4. AdaBoost  
5. Support Vector Machine (SVM)  
6. K-Nearest Neighbors (KNN)  
7. Naive Bayes  
8. Decision Tree  
9. XGBoost  
10. LightGBM  
11. CatBoost  

**Top Models per Dataset Type**:  
- **Normal Data**:
  - Gradient Boosting: F1 = 0.611872  
  - Random Forest: F1 = 0.584235  
  - CatBoost: F1 = 0.591463  

- **Oversampled Data (SMOTE)**:
  - CatBoost: F1 = 0.808713 ✅ Best Overall  
  - LightGBM: F1 = 0.795393  
  - XGBoost: F1 = 0.787676  

- **Undersampled Data**:
  - CatBoost: F1 = 0.759494  
  - Gradient Boosting: F1 = 0.744544  
  - LightGBM: F1 = 0.744304  

---

## Best Model: CatBoost (Oversampled Data)
- **F1-Score**: 0.8087 (before hyperparameter tuning).  
- **Classification Report**:
  - Precision: 88%  
  - Recall: 75%  
  - Accuracy: 88%  

### Confusion Matrix (Before Tuning):
| Actual\Predicted | Not Churn | Churn |
|------------------|-----------|-------|
| **Not Churn**    | 1514      | 79    |
| **Churn**        | 202       | 594   |

---

## Business Recommendations
### **1. Address High-Churn Age Groups:**
- **Older Customers**: Provide personalized communication, financial advisory services, or exclusive offers.
- **Younger Customers**: Implement onboarding programs to engage customers with low tenure, such as gamified milestones.

### **2. Focus on Low-Tenure Customers:**
- Offer loyalty incentives like welcome discounts or milestone-based rewards for early retention.

### **3. Improve Retention for Low-Balance Customers:**
- Introduce flexible payment plans or rewards for increasing account balances.

### **4. Tailor Strategies Based on Country Segmentation:**
- Develop country-specific campaigns for Spain and Germany with localized messaging and culturally relevant offers.

### **5. Enhance Engagement for Low Product Usage:**
- Cross-sell or bundle relevant products to encourage customers to expand their usage.

### **6. Leverage High CLV Segments (VIP & High):**
- Provide premium services, tiered loyalty benefits, and upselling opportunities for high-value customers.

### **7. Promote Balanced Spending:**
- Encourage medium-CLV customers to move to higher tiers by offering exclusive rewards.

### **8. Increase Tenure for Higher CLV:**
- Launch campaigns promoting long-term contracts and time-based loyalty rewards.

### **9. Monitor Credit Score Impact:**
- Offer financial education programs or personalized financial advice to low-credit-score customers.

### **10. Incentivize Product Expansion:**
- Promote bundled packages or discounts for adding multiple products to increase customer value.

---

## Conclusion
This project demonstrates how machine learning models and CLV analysis can provide actionable insights for reducing churn and optimizing customer profitability. The **CatBoost model** trained on oversampled data emerged as the best predictor, offering a balanced approach to precision and recall. These insights can empower the bank to implement targeted retention strategies, foster customer loyalty, and maximize long-term profitability.

