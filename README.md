# Marketing Campaign
* Built a classification model with 80% accuracy and an F1-score of 0.49 on the test data to predict customer acceptance of a marketing campaign.
* Identifying customers who are more likely to accept the campaign will assist companies in using their marketing resources more effectively.
* Cleaned and conducted data exploration on 2,240 observations and 29 columns (2 categorical, 1 date type, and the remaining 26 were numerical) from https://www.kaggle.com/rodsaldanha/arketing-campaign.
* Compared model performance on a standard original dataset and a standardized dataset that was balanced using Synthetic Minority Oversampling Technique (SMOTE) and Random Undersampling. 
* Used GridSearchCV to identify the best parameters on seven different classification models.
* Compared nine different classification metrics, including an engineered profit metric. 
* The two best models were selected and evalauted on the set aside test data. Results indicate the **Random Forest Classifier** produced the best overall metrics, including the highest profit score.

## Code and Resources Used
**Packages:** numpy, pandas, seaborn, matplotlib, sklearn

## Data Cleaning
Data included 2,240 observations and 29 columns.
* Examined missing values and addressed 24 missing income values using scikit-learn's Iterative Imputer function.
* Examined distribution of categorical and numeric variables.
* Engineered features, including total amount spent, total number of purchases, total number of minors in the home, and total number of campaigns previously accepted.
* Removed one income outlier.

## Data Exploration
Examined the frequencies of cateogorical variables and the distributions and relationships between numeric variables.

![Histograms of Movies Variables](https://github.com/chelseako/ml_recommender_system/blob/main/movie.png)

![Histograms of Users Variables](https://github.com/chelseako/ml_recommender_system/blob/main/user.png)

## Model Building  
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

## Model Performance

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

## Results

Using profit as the main evaluator, the **Random Classifier** and the **Logistic Regression Classifier** were chosen as the two best models. These two models were evaluated on the set aside test data. Results indicate the **RandomForest Classifier** produced the best overall metrics, including the highest profit score.
