# Time Series Analysis: ROC-AUC Comparison Across Models

This repository presents a time series analysis of predictive models, comparing their **ROC-AUC** performance over time across **train**, **test**, and **validation** sets.


# Data Preprocessing and Feature Aggregation
The dataset used in this project contains time-series data of 3D tumor spheroids. Each sample belongs to one of two target categories:

*Relapsed*: Tumor spheroids that relapsed after treatment.
*Controlled*: Tumor spheroids that remained controlled after treatment.

## Procedure Overview:
### Feature Aggregation:
The dataset includes multiple observations recorded at different time points (days), such as day 0, 3, 5, 7, 10, 12, and 14.
To aggregate these features into a single row per sample, we use a pivot table to organize the features across the different days.
Each feature is split by the day it was recorded, resulting in columns such as feature1_day0, feature1_day3, feature1_day5, and so on. This allows the model to consider how features evolve over time when predicting the outcome.
### Merging the Aggregated Features with Target Labels:

After aggregating the features for each tumor spheroid (or well), the dataset is merged with the corresponding target labels, and diagnosis. The target labels (relapsed vs controlled) are stored separately and merged back with the features based on the well (tumor spheroid sample).
This results in a single dataframe where each row represents one tumor spheroid sample, with all the day-specific features and the target label.

## Model Training:

After preparing the features and target variable, the dataset is ready for training machine learning models.
In this case, no balancing techniques are applied, as the dataset is sufficiently balanced between the two target categories (relapsed and controlled).
The models are trained using the time-series data, where the evolution of features over different days is considered for making predictions.

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
