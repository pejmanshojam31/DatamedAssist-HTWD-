# Update on the work
In the previous update, we saw a big gap between the train and test data (92% to 72%) for the Lasso feature selector and Gradient Boosting ML method. Figure.1 shows this gap in a time-dependent plot.
<img src="https://github.com/user-attachments/assets/b0c3824a-bc98-4791-9277-2eb5e1588e58" width="500"/>
Therefore, I first combined the dataset and then splitter it based on five different folds to check how it affects the outcome and whether we see the previous pattern again. Suprisingly, the model works perfectly on both the train and test sets, implying that the previous test set was not a good candidate for testing the model. 
<img src="https://github.com/user-attachments/assets/9eed4d75-9b5a-42df-8ceb-ed62f5b46164" width="500"/>

In more detail, figure. 3 shows the differences between the train and test set of one of those folds. 

<img src="https://github.com/user-attachments/assets/fe6f50e9-1ea8-4237-bbaf-a462941a9cf1" width="500"/>

In conclusion, I would say the model works properly for the test set. 

