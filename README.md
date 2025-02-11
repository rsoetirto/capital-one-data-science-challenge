# Credit Card Fraud Detection – Capital One Data Science Challenge

## Overview
This project aims to detect fraudulent transactions using **Logistic Regression, Random Forest, and XGBoost**. The dataset is imbalanced, requiring advanced resampling techniques and optimized models to improve fraud detection.

## Model Selection
Three models were chosen for evaluation:

- **Logistic Regression**: Baseline model for interpretability and efficiency.
- **Random Forest**: Ensemble method that captures non-linear patterns and reduces overfitting.
- **XGBoost**: High-performance boosting algorithm that handles imbalanced data effectively.

## Data Preprocessing
- **Handled class imbalance** using **SMOTE and SMOTEENN**.
- **Feature scaling and encoding** applied to improve model performance.
- **Engineered new features** (e.g., transaction time patterns, rapid transaction flags).

## Model Performance Comparison
| Model             | Accuracy | Precision | Recall | F1 Score | ROC AUC |
|------------------|----------|-----------|--------|----------|---------|
| **Logistic Regression** | 75%  | 0.77      | 0.76   | 0.77     | 0.832   |
| **Random Forest**       | 99%  | 1.00      | 0.98   | 0.99     | 0.998   |
| **XGBoost**            | 88%  | 0.82      | 1.00   | 0.90     | 0.997   |

## ROC Curves
- **Logistic Regression ROC AUC**: `0.832`
- **Random Forest ROC AUC**: `0.998`
- **XGBoost ROC AUC**: `0.997`

<img src="roc_curve_log_reg.png" width="300"> <img src="roc_curve_rf.png" width="300"> <img src="roc_curve_xgb.png" width="300">

## Key Insights:
- **Random Forest** had **almost perfect precision and high recall**, making it ideal for fraud detection.
- **XGBoost** was **more aggressive** (higher recall, 98.7%), but **flagged more false positives** (legitimate transactions wrongly marked as fraud).
- **Logistic Regression** performed **moderately well**, but struggled to distinguish fraud effectively.

## **Final Recommendation**
**Random Forest** is the best model because it achieves **both high recall (98%) and perfect precision (100%)**, minimizing false positives and false negatives.

## Future Improvements
- **Threshold tuning** to balance fraud detection and minimize customer inconvenience.
- **Incorporate deep learning models** (e.g., LSTMs for sequential transaction data).
- **Real-time fraud detection pipeline** with continuous model updates.

---

### **How to Run the Model**
1. Clone the repository:
   ```bash
   git clone https://github.com/rsoetirto/capital-one-data-challenge.git

