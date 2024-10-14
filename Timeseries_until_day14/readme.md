# Time Series Analysis: ROC-AUC Comparison Across Models

This repository presents a time series analysis of predictive models, comparing their **ROC-AUC** performance over time across **train**, **test**, and **validation** sets.

## Models Used

The following models were used:
- **Random Forest**
- **Logistic Regression**

## Results

### 1. Random Forest Performance

**Generalization**: Random Forest performs well on both the test and validation sets...

### 2. Logistic Regression Performance

_Logistic Regression shows signs of overfitting..._

## Recommendations

1. **Random Forest**: Strong candidate for further refinement...
2. **Logistic Regression**: Consider adjusting regularization parameters...

## Visualization

<img src="https://github.com/user-attachments/assets/fbe7396e-daae-4ac9-b3bc-9d753bd1344d" alt="Download (1)" width="600"/>

## Key Results
1. Random Forest Performance
Generalization: Random Forest performs well on both the test and validation sets, showing little to no overfitting. The train, test, and validation ROC-AUC values remain closely aligned across all days.
Consistency: The model’s performance improves as more days are added (up to day 10-12), with little gain beyond this point, suggesting the model has learned the key patterns by day 10.
Conclusion: Random Forest is a strong candidate for this problem, with excellent generalization and stability over time.
2. Logistic Regression Performance
Overfitting: Logistic Regression shows signs of overfitting—the train AUC is significantly higher than the test and validation AUCs, especially in the early days.
Test/Validation AUC: The model's performance improves with more data, but it struggles to match Random Forest’s test and validation performance. By day 10, the test and validation AUCs stabilize but remain lower than the training AUC.
Conclusion: Logistic Regression may not be the best choice for this problem due to its tendency to overfit and its lower generalization performance.
