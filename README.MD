### Supervised Machine Learning - Predicting Credit Risk


#### Background
LendingClub is a peer-to-peer lending services company that allows individual investors to partially fund personal loans as well as buy and sell notes backing the loans on a secondary market. LendingClub offers their previous data through an API.
The data is used to create machine learning models to classify the risk level of given loans. Specifically, comparison is made between the Logistic Regression model and Random Forest Classifier.

#### Retrieve the data
In the Generator folder in Resources, there is a GenerateData.ipynb notebook that will download data from LendingClub and output two CSVs:

- 2019loans.csv
- 2020Q1loans.csv

An entire year's worth of data (2019) is used to predict the credit risk of loans from the first quarter of the next year (2020).
Note: these two CSVs have been undersampled to give an even number of high risk and low risk loans. In the original dataset, only 2.2% of loans are categorized as high risk. To get a truly accurate model, special techniques need to be used on imbalanced data. Undersampling is one of those techniques. Oversampling and SMOTE (Synthetic Minority Over-sampling Technique) are other techniques that are also used.

#### Preprocessing: Convert categorical data to numeric
Created a training set from the 2019 loans using pd.get_dummies() to convert the categorical data to numeric columns. Created a testing set from the 2020 loans, also using pd.get_dummies(). Filled the missing categories in the testing set.

#### LogisticRegression model

#### RandomForestClassifier model
