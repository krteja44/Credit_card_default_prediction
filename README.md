# credit_card_default_prediction  
### Credit department in a bank is a leading data science adopter. Acquiring new credit card users is always a key priority for the bank. Giving credit cards without due diligence or assessment for creditworthiness is a huge risk. In the analysis, we will use the AdaBoost method and some other algorithms for predicting credit card approval decisions.

The data is sourced into two files. 
- application_record: This file consists of application data used for feature creation.
- credit_record: This file consists of monthly credit card account status information and the status (credit payment status) will be required for defining the labels - which of the applications have paid back dues and which of these turn out to bad accounts.  

### 1. Exploratory Data Analysis
#### Observations: 
- Around 67.14% of the applicants are female
- Housing ownership percentage for females is 90.89% while for males it is 87.58%. Females applicants have higher house ownership percentage.
- It is certain that the average income increases with the education level.
### 2. Feature Elimination
#### Used Weight of Evidence and Information Value to retrieve the top features which accounts for greater accuracy in financial data.
- Weight of Evidence (WoE) is a measure of the “strength” of a grouping technique to separate good and bad. This method was developed primarily to build a predictive model to evaluate the risk of loan default in the credit and financial industry.
- Information Value (IV) measures the importance of a feature and depends only on frequency counting and does not need to fit a model to obtain an attribute importance score
### 3. Model Building
- Used Logistic regression, Decision Trees and AdaBoost algorithms 
- Eliminated less variant features using Information Values
### 4. Hyperparameter Tuning
- Decision Tree and AdaBoost Best Parameters: {'criterion': 'gini',
 'max_depth': 5,
 'min_samples_leaf': 50,
 'min_samples_split': 50}
### 5. Conclusion Thoughts and Future Work:
- Using AdaBoost algorithm gave us a good accuracy level.
- Model is deployed onto Amazon ECR to serve as an endpoint to the business users.
- Further, model needs to be evaluated and updated based on Users feedback with a 2 month period data. 
