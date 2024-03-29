# Census-Income-Predictor
Task : Whether a person make over 50K a year or not.
Notebook Link: https://www.kaggle.com/code/raaggeesingh/census-income-dataset-88-accuracy

# 1. What approach I used to solve the task?
I used the classical Vote Classification algorithm. Vote Classification is a machine learning algortihm which combines multiple machine learning algorithms and then predicts the output based on highest probability of chosen class. 

# 2. What were the ensemble machine learning models which I used?
I ensembled Random Forest Classifier, Gradient Boost Classifier and XGBClassifier.

# 3. What does the procedure looks like?
1. Data Preprocessing: Checking and dropping null value. Dataset also has an ambigous value "?". I replaced it with NaN and removed those values.
2. EDA: Performed extensive EDA and finding all relations between the columns
3. Feature Engineering: Converting people earning >=50K and <50K into labels. Also encoding all the categorical features into labels.
4. Machine Learning model and Fine Tuning:
   a. Initially used RobustScaler to scalerize all the numerical values.
   b. Divided the dataset into training and testing
   c. Defined parameters of Random Forest Classification, Gradient Boost Classifier and XGBClassifier and applied optuna for Hyperparameter Tuning.
   d. Ensembled the models with Vote Classifier with the parameters generated by Hyperparameter Tuning and then applied KFold to check the accuracy of the model on the dataset.
   e. Finally predicted the model on test datatset and achieved accuracy score of 88%.
