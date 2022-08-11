# Fetal Health Classification
Classify the health of a fetus as Normal, Suspect or Pathological using CTG data

Data
This dataset contains 2126 records of features extracted from Cardiotocogram exams, which were then classified by three expert obstetritians into 3 classes:
•	Normal
•	Suspect
•	Pathological

Project Solution
1) Handing missing values and duplicate records -
I check for the NA values using .isna() function , removed the duplicates using data.drop_duplicated()
2) Data Imbalance -
Here the 'y' ie. our dependent variable to be predicted had 3 classes were one of the class had very high value count respective to other so to handle this I used the oversampling technique that would fix the problem of data imbalance.
3) Multicollinearity -
Here some the independent features are correlated to each other and must be removed from the dataset while predicting for dependent variable , I used the VIF technique to remove the highly correlated variable.
4) Finding the perfect model fit
Now to create a model I splitted the data into train and test set , next I fitted the Logistic Regression and LDA and tested on the test dataset.
Now to increase the model accuracy I did hyperparameter tuning on both the models using GridSearchCV.
Then I used LGBM (Light Gradient Boosted Machine) algorithm to check how it works on the data.
Final Results - Logistic Regression 78% accuracy , LDA 82% accuracy , LGBM - 95 % accuracy.
