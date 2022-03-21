# Marketing Campaign
* Built a classification model with 80% accuracy and F1-score of 0.49 on the test data to predict customer acceptance of a marketing campaign.
* Identifying customers who are more likely to accept the campaign will assist companies in using their marketing resources more effectively.
* Cleaned and conducted data exploration on 2,240 observations and 29 columns.

Compared model performance on two datasets: 
1. A standardized dataset
2. A standardized dataset that used Synthetic Minority Oversampling Technique (SMOTE) and Random Undersampling to address class imbalance.

Used GridSearchCV on the following models to determine the best parameters: 
* Logistic Regression
* Support Vector Machines
* KNN
* Decision Tree
* Random Forest
* Adaboost
* Gradient Boosting

Used the following evaluation metrics:
* Training accuracy
* Validation accuracy
* Recall
* Specificity
* Precision
* Balanced Accuracy
* F1 score
* Difference between training and validation accuracy
* Profit

The dataset indicated that each contact cost the company \$3, and each campaign acceptance produced a revenue of \$11. Using this data, we calculated the following profit evaluation metric:  

Profit = (True positives x \$11 revenue) - (False positives x \$3 cost) - (False negatives x \$11 lost revenue)

Using profit as the main evaluator, the **Random Classifier** and the **Logistic Regression Classifier** were chosen as the two best models. These two models were evaluated on the set aside test data. Results indicate the **RandomForest Classifier** produced the best overall metrics, including the highest profit score.
