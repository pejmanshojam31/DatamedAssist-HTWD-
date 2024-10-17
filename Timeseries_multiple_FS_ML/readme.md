# Update 17.10.24
## Using the external dataset to check the model performance using multiple feature selectors and machine learning models.
In this section, I used the external dataset to check the model performance and try to tackle the problems. I had to change the feature names in this external dataset, since it used the uppercase alphabet. 

# Results show a different accuracy but promising.
The **Lasso + Logistic Regression model** appears to have performed the best overall on this external dataset, while SVC models consistently perform poorly.
Feature selection using **PCA** and **Lasso** seem to yield more stable and competitive results across models.


<img src="https://github.com/user-attachments/assets/7bd5325c-3275-462a-94ee-3d48d2421a91" width="500"/>

**Lasso + Logistic Regression** shows more balanced and reliable performance, even though the external dataset results are lower, indicating that this combination may be more robust for future external validation.
The fluctuations in **Random Forest** on the external dataset suggest it may be more sensitive to data variance or noise, despite performing exceptionally well on the validation set.

<img src="https://github.com/user-attachments/assets/d1dd0b87-1f5f-4bc0-a466-09dda4e0a919" width="600"/>

# What Can You Do Now?
Domain Adaptation: You could explore domain adaptation techniques to adjust for any distribution shifts between the training/validation and external datasets.
Feature Robustness Analysis: Investigate the robustness of radiomic features across datasets by checking for feature stability under different acquisition or preprocessing conditions.
Ensemble Approaches: If the external dataset presents more variability, ensemble models that combine multiple classifiers or feature selection methods might help improve generalization.
