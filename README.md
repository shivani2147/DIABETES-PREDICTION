# Diabetes Prediction
- This dataset originates from the National Institute of Diabetes, Digestive and Kidney Diseases, a reputable health institute.
- The primary objective of this dataset is to predict whether a patient has diabetes based on various test results and health indicators.
- It serves as a valuable resource for healthcare professionals and data scientists to develop predictive models and algorithms aimed at early detection and management of diabetes.
- It includes various features such as glucose levels, blood pressure, body mass index (BMI), and other medical indicators commonly associated with diabetes.
- By leveraging machine learning algorithms on this dataset, researchers aim to enhance diagnostic accuracy and provide early intervention for individuals at risk of diabetes.

### Columns Include : 
- Pregnancies --> Number of times pregnant
- Glucose --> Plasma glucose concentration a 2 hours in an oral glucose tolerance test
- BloodPressure --> Diastolic blood pressure (mm Hg)
- SkinThickness --> Triceps skin fold thickness (mm)
- Insulin --> 2-Hour serum insulin (mu U/ml)
- BMI --> Body mass index (weight in kg/(height in m)^2)
- DiabetesPedigreeFunction --> Diabetes pedigree function
- Age --> Age (years)
- Outcome --> Class variable (0 or 1)

--- 
### Through this analysis, I seek to understand the following:
1. It's a Classification based task
2. There are 768 records and 9 features
    - "Outcome" is the Target feature
3. No null values or duplicate values found
4. Types of data are Numerics only
5. Number of Non-Diabetic patients are 500 (65%) and Diabetic patients are 268 (35%).
6. Outliers found in [Pregnancies, Glucose and Skin Thickness]
    - Identified row number and then removed
7. Skewness Found :
    - Checked the distribution with the help of histplot visualization
    - Checked the one by one Skewness
    - Checked the correlation
    - Checked if there's any negative value
    - Applied lock transformation to [Glucose, DiabetesPedigreeFunction and Age]
8. Split Input Features and Output Target from the dataset
9. Applied StandardScalar on Input features (fit_transform)
10. Split the data into 80% and 20%
11. Created Baseline Model
    - Train, Test / Predict, Confusion Matrix, Classification Report, Accuracy
12. Logistic Regression
    - Accuracy - 81.58% 
13. Decision Tree Classifier
    - Accuracy - 75.66%
    - Check Feature Importances and created a Tree to visualise it
    - Here, "Glucose" is the most information feature
14. Pruning Technique
    - Entropy (max_depth = 4) --> Accuracy - 75.0%
    - Entropy (min_samples_leaf = 50) --> Accuracy - 73.03%
    - Here, Glucose, BMI & Age feature are important
15. Ensembling Technique :
    - Random Forest Classifier --> Accuracy - 76.32%
    - Ada Boost Classifier --> Accuracy - 80.26%
    - Gradient Boosting --> Accuracy - 70.39%
    - Extreme Gradient Boosting --> Accuracy - 81.58%
16. K-Nearest Neighbor (KNN)
    - Accuracy - 81.58%
17. Support Vector Machine
    - Linear --> Accuracy - 81.58%
    - Non-Linear :
      - Polynomial Kernel Function --> Accuracy - 81.58%
      - Radial Basis Kernel Function --> Accuracy - 81.58%
