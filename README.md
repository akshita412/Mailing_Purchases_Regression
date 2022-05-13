# Project Overview
This project repository is created to predict the purchasing amount of customers who have been part of a mailing campaign. 

## Key Question
The data contains information about whether or not different consumers made a purchase in response to a test mailing of a certain catalog and, in case of a purchase, how much money each consumer spent. How do different regressors perform when:
- all customers who were sent the mail are taken for analysis
- only the customers who purchased are taken for analysis

## Dataset
The dataset is a custom dataset consisiting of 25 columns with 16 binary variables depicting the source. Other columns are gender, total days before last update, purchasing flag, etc. 
The dataset has been uploaded to the repository.


## Approach
- Some initital EDA and anomaly detection checks are performed, correlation was checked.
- Different regressors performances were observed. The regressors were:
    - Linear
    - KNN
    - Decision Tree
    - SVR
    - Random Forest
    - XGBoost
    - LightGBM
- The performance on the above models was again observed after implementing nested cross validation
- Neural network regressors were also implemented, yielding decent performance.
- Next, all the above steps were carried out by taking the alternate dataset, i.e. only the users who made a purchase were considered for numeric prediction problem.

## Results
Model comparison for both datasets indicated that the ensemble models performed better than other models. But Neural network performs the best in both cases.

But, RMSE was lesser for first dataset compared to second dataset for neural network. This is happening becuase when all purchases are 1 then model is overfitting on test data and is not able to generalize the behaviour that well.
