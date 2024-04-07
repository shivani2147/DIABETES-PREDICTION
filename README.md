# Diabetes Prediction
- This dataset originates from the National Institute of Diabetes, Digestive and Kidney Diseases, a reputable health institute.
- The primary objective of this dataset is to predict whether a patient has Diabetes based on various test results and health indicators.
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
1. It's a classification-based task.
2. The dataset comprises 768 Records and 9 Features, with "Outcome" serving as the Target feature.
3. No null or duplicate values were detected, and the data types are exclusively numeric.
4. Out of the total, 500 (65%) patients are Non-Diabetic, while 268 (35%) are Diabetic.
5. Outliers were identified in "Pregnancies," "Glucose," and "Skin Thickness" features, and corresponding rows were removed.
6. Skewness Found :
    - Analyzed distribution using Histogram plots.
    - Assessed skewness individually.
    - Examined correlation.
    - Checked if there's any negative value.
    - Applied logarithmic transformation (log()) to 'DiabetesPedigreeFunction', and 'Age'.
7. The dataset was split into Input features and Output target
8. Applied StandardScalar on Input features 
9. Data was split into 80% Training and 20% Testing sets.
10. A Baseline Model was created, including Training, Testing / Predicting, Confusion Matrix generation, Classification Report, Accuracy
11. Logistic Regression achieved an accuracy of 81.58%.
12. Decision Tree Classifier achieved an accuracy of 75.66%, with Feature Importances examined and a visualization created by creating a Tree like structure.
    - Here, "Glucose" is the most information feature
13. Pruning Techniques were applied with varying parameters, resulting in accuracies of 75.0% (max_depth = 4) and 73.03% (min_samples_leaf = 50), highlighting the importance of "Glucose," "BMI," and "Age" features.
14. Ensemble Techniques such as Random Forest Classifier (76.32%), AdaBoost Classifier (80.26%), Gradient Boosting (70.39%), and Extreme Gradient Boosting (81.58%) were implemented.
15. K-Nearest Neighbor (KNN) achieved an accuracy of 81.58%.
16. Support Vector Machine (SVM) achieved an accuracy of 81.58% for both Linear and Non-Linear (Polynomial and Radial Basis) Kernel Functions.
