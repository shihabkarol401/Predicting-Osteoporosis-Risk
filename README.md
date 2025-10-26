# Predicting Osteoporosis Risk
This project focusses on predicting osteoporosis risk using patient medical, lifestyle, and demographic data. It integrates clinical insights with advanced machine learning techniques, culminating in a finely tuned XGBoost Classifier that delivers high accuracy and reliability in identifying individuals at risk for osteoporosis.

# Project Workflow
1. Data Preparation: Loaded the dataset, handled missing values in Alcohol Consumption, Medical Conditions, and Medications using mode imputation, and dropped irrelevant columns such as Id.
2. Exploratory Data Analysis (EDA): Identify patterns and relationships in the dataset.
3. Feature Engineering: Created an interaction term between 'Age' and 'Smoking_Yes' to capture potential combined effects and one-hot encoded categorical variables for model compatibility.
4. Data Splitting and Scaling: Split the dataset into 80% training and 20% testing sets and applied StandardScaler to normalize numerical features for consistent model input.
5. Data Balancing: Addressed class imbalance using SMOTE (Synthetic Minority Over-sampling Technique) to generate synthetic samples for the minority class, ensuring balanced model learning.
6. Model Training: Trained multiple classification models — Logistic Regression, Decision Tree, Random Forest, SVM, Naïve Bayes, KNN, Gradient Boosting, and XGBoost — to compare predictive performance.
7. Model Evaluation: Compare model performance metrics.
8. Model Selection: Select the model with the highest AUC-ROC and precision scores.
9. Hyperparameter Tuning: Bayesian Optimization used to fine-tune XGBoost hyperparameters, maximizing ROC-AUC and enhancing generalization performance.

# Dataset Description
The dataset includes related data for osteoporosis risk prediction:
1. ID: Unique identifier for each patient.
2. Age Age of the patient.
3. Gender: Gender of the patient.
4. Hormonal Changes: Whether the patient has undergone hormonal changes.
5. Family History: Whether the patient has a family history of osteoporosis.
6. Race/Ethnicity: Race or ethnicity of the patient.
7. Body Weight: Weight details of the patient.
8. Calcium: Calcium levels in the patient's body.
9. Vitamin D: Vitamin D levels in the patient's body.
10. Physical Activity: Physical activity details of the patient.
11. Smoking: Whether the patient smokes.
12. Alcohol Consumption: Whether the patient consumes alcohol.
13. Medical Conditions: Medical conditions of the patient.
14. Medication: Medication details of the patient.
15. Prior Fracture: Whether the patient has had a prior fracture.
16. Osteoporosis: Whether the patient has osteoporosis.

# Exploratory Data Analysis (EDA)
The EDA phase involves:
1. Conducted visual analysis to understand the distribution of key features.
2. Identified correlations between numerical variables using heatmaps and pair plots.
3. Examined the relationship between lifestyle factors (e.g., smoking, alcohol consumption, physical activity) and osteoporosis risk.
4. Analyzed demographic influences such as age, gender, and ethnicity on osteoporosis occurrence.
5. Investigated the impact of medical factors (e.g., existing conditions, medications) on the likelihood of developing osteoporosis.

# Model Selection and Evaluation
Evaluated multiple models using AUC-ROC:
1. Logistic Regression: AUC-ROC = 0.8765
2. Decision Tree: AUC-ROC = 0.8209
3. Random Forest: AUC-ROC = 0.8883
4. Support Vector Classifier: AUC-ROC = 0.8774
5. Gaussian Naïve Bayes: AUC-ROC = 0.8613
6. K-Nearest Neighbors: AUC-ROC = 0.7897
7. Gradient Boosting: AUC-ROC = 0.8894
8. XGBoost: AUC-ROC = 0.8965

XGBoost Classifier was selected due to its superior AUC-ROC performance. Bayesian Optimization further enhanced its results.

# Model Performance
1. XGBoost model delivered an Accuracy of 0.8852, indicating strong overall predictive capability.
2. Attained a Precision of 1.0000, meaning all positive predictions were correct.
3. Achieved a Recall of 0.7704, effectively identifying most true osteoporosis cases.
4. Reached an F1-Score of 0.8703, balancing precision and recall performance.
5. Recorded a ROC-AUC score of 0.9003, demonstrating excellent class discrimination ability.
6. The confusion matrix and ROC curve confirmed consistent and reliable model performance on the test set.
