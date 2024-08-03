Overview:
This project aims to predict whether a person has diabetes using machine learning. It leverages a dataset containing various medical attributes to train a model and evaluate its performance. Furthermore, it incorporates explainable AI techniques to interpret the model's predictions.

Dataset:

The dataset used in this project contains the following attributes:
ID: Patient ID
Pregnancies: Number of times pregnant
Glucose: Plasma glucose concentration a 2 hours in an oral glucose tolerance test
BloodPressure: Diastolic blood pressure (mm Hg)
SkinThickness: Triceps skin fold thickness (mm)
Insulin: 2-Hour serum insulin (mu U/ml)
BMI: Body mass index (weight in kg/(height in m)^2)
DiabetesPedigreeFunction: Diabetes pedigree function
Age: Age (years)
Gender: Gender of the patient
Chol: Cholesterol level
No_Pation: (Note: This column will be dropped as it is non-predictive)
CLASS: The class labels in the dataset are as follows:
        N
        N (with a trailing space)
        P
        Y
        Y (with a trailing space)
It seems like there might be some inconsistencies, such as trailing spaces. These need to be cleaned up to ensure the class labels are properly interpreted.
N: No
P: Positive
Y: Yes

Steps:
Import Libraries: Import necessary libraries for data manipulation, preprocessing, machine learning, and visualization.
Load Dataset: Load the dataset from a CSV file.
Initial Exploration: Perform initial exploration to understand the dataset's structure, including displaying the first and last few records, statistical summary, shape, column names, data types, unique values, and missing values.
Encoding Categorical Variables: Convert categorical variables (e.g., Gender) to numerical values using label encoding.
Drop Non-Predictive Columns: Remove columns that do not contribute to the prediction (e.g., ID, No_Pation).
Scaling: Scale the features to have a mean of 0 and a standard deviation of 1 using StandardScaler.
Correlation Matrix: Calculate and visualize the correlation matrix to understand relationships between features.
Train-Test Split: Split the dataset into training and testing sets.
Hyperparameter Tuning: Use GridSearchCV to find the best hyperparameters for the RandomForestClassifier.
Model Training: Train the RandomForestClassifier using the best parameters obtained from GridSearchCV.
Model Evaluation: Evaluate the model's performance using accuracy, precision, recall, and F1 score.
Predictions: Make predictions on the test set and display sample predictions.
Explainable AI (XAI): Use LIME to explain the model's predictions for individual instances.
