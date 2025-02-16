# House-Price-Prediction

Objective
This notebook is designed to predict real estate prices using machine learning. The dataset used consists of various housing features and the target variable, MEDV (Median Value of Owner-Occupied Homes in $1000s).

1. Data Loading & Exploration
The dataset contains 506 entries and 14 columns.
Features include crime rate (CRIM), number of rooms (RM), tax rates (TAX), and more.
Missing values found: 5 missing values in RM (Number of rooms per dwelling).
First Five Rows of Data:
CRIM	ZN	INDUS	CHAS	NOX	RM	AGE	DIS	RAD	TAX	PTRATIO	B	LSTAT	MEDV
0.006	18	2.31	0	0.538	6.575	65.2	4.090	1	296	15.3	396.9	4.98	24.0
0.027	0	7.07	0	0.469	6.421	78.9	4.967	2	242	17.8	396.9	9.14	21.6
0.027	0	7.07	0	0.469	7.185	61.1	4.967	2	242	17.8	392.8	4.03	34.7
0.032	0	2.18	0	0.458	6.998	45.8	6.062	3	222	18.7	394.6	2.94	33.4
0.069	0	2.18	0	0.458	7.147	54.2	6.062	3	222	18.7	396.9	5.33	36.2
2. Train-Test Splitting
The dataset is split into 80% training data and 20% test data using train_test_split from scikit-learn.
This ensures the model is trained on a subset of data while keeping unseen data for evaluation.
3. Data Preprocessing
Handling missing values: Missing values in RM are replaced with the median.
Feature scaling: Standardization is applied to numerical features to improve model performance.
Pipeline Creation: Data transformations are applied using scikit-learn Pipelines for efficiency.
4. Model Training & Evaluation
Multiple models are trained to predict house prices:

Model	Performance (RMSE)
Linear Regression	Moderate Accuracy
Decision Tree	Overfits Training Data
Random Forest	Best Performance
Random Forest performed the best, achieving lower errors due to its ability to reduce overfitting.
Cross-validation was used to improve model reliability.
5. Predictions & Model Deployment
The best-performing model is saved using Joblib (Dragon.joblib).
Predictions are tested on new, unseen data.
