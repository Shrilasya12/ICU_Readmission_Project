Predicting 30-Day ICU Readmissions Using the MIMIC-III Dataset This project focuses on building a machine learning model to estimate the likelihood of a patient being readmitted to the ICU within 30 days of discharge. The analysis is based on the MIMIC-III clinical database, which contains anonymized health data from ICU stays.

Overview The main objective was to identify patterns in patient health records that could help predict early readmissions, enabling proactive medical interventions.

The workflow included:

Extracting and preprocessing patient data from MIMIC-III

Engineering features relevant to readmission risk

Training and optimizing a machine learning classifier

Evaluating performance using multiple metrics and visualizations

Data Source The MIMIC-III database contains detailed records from approximately 60,000 ICU admissions for around 40,000 unique patients over a 10-year span. 🔗 MIMIC-III Website

To run this project:

Install and configure a local PostgreSQL server.

Set up the MIMIC-III database as described in the MIT-LCP build guide.

Use the provided all_data.sql script to create a materialized view for analysis.

Tools & Libraries numpy – numerical operations

pandas – data manipulation

os – file and system handling

psycopg2 – PostgreSQL database connection and queries

xgboost – gradient boosting classifier

scikit-learn – model evaluation, hyperparameter tuning

scipy – utilities for ROC curve plotting

matplotlib & seaborn – data visualization

Key Results Before Preprocessing – Numerical Features Scatter Matrix A: Scatter matrix of all numerical features. B: Zoom-in on the first 6 features. The diagonal displays KDE plots for each feature.

After Preprocessing – Numerical Features Scatter Matrix A: Scatter matrix of all numerical features after cleaning and scaling. B: Zoom-in on the first 6 features.

ROC Curve – Optimized Model (5-Fold Cross Validation)

Feature Importance A: Features ranked by weight in the XGBoost model. B: KDE plots for the top 9 most important features by class label.

Summary By leveraging clinical data from MIMIC-III and applying a gradient boosting approach, the model can effectively estimate the probability of ICU readmission within 30 days. These insights can support healthcare providers in identifying high-risk patients and reducing preventable readmissions.
