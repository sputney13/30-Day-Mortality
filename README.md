# 30-Day Mortality Prediction for Hospital Admissions
*Duke University BME590 Data Science and Health Final Project*

This project utilized data from the MIMIC-III Clinical Database, a database containing health data for over forty thousand patients who stayed in critical care units of the Beth Israel Deaconess Medical Center between 2001 and 2012, to create a predictive model for 30-day mortality. Each eligible hospital admission was flagged if the patient died within 30 days of the admission date, and various factors in the patients' stay served as variables for fitting a predictive model to the data. Because a predictive model for 30-day mortality is primarily useful in the early stage of an admission (before an at-risk patient would die), data used as variables for modeling were limited to static information obtained at the patient's admission time. Though other data obtained within the first 24 hours of a patient's stay (for example, chart data or lab results) may also prove predictive of 30-day mortality rate, the purpose of this model is to attempt to flag new admissions as likely (or unlikely) to die within 30 days of admission at the moment they are admitted to the hospital. Assessment of the model considered its ROC-AUC score, precision-recall score, and accuracy, compared against a benchmark model that predicts no occurences of 30-day mortality.

**Table of Contents**
1. Overview & Background
2. Data
    1. Admissions
    2. Patients
    3. Creating the 30-Day Mortality Label
    4. Diagnosis ICD-9 Codes
    5. ICU Stays
    6. Summary of Cleaned Data
3. Exploratory Data Analysis
4. Modeling
    1. Creating the Model Matrix
    2. Training for Hyperparameters
        1. Logistic Regression Model
        2. Gradient Boosting Classifier
    3. Variable Selection with 5-Fold Cross Validation
        1. Logistic Regression Model (C=1.0)
        2. Gradient Boosting Classifier (max_depth = 4)
    4. Summary Statistics for Models
5. Suggestions
6. Conclusions
7. Resources
