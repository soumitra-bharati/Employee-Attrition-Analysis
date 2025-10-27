# Employee Attrition Prediction & Analysis
This project analyzes the IBM HR Analytics Employee Attrition dataset to identify key factors that drive employee turnover. It includes a comprehensive exploratory data analysis (EDA), the development of a predictive machine learning model, and a set of data-driven recommendations for retention strategies.


### Dataset 
- The analysis uses the public IBM HR Analytics Employee Attrition dataset from Kaggle.
- It comprises 1,470 employee records with 35 features.
- The target variable, Attrition, is binary ("Yes"/"No") and shows a severe class imbalance, with 84% of employees retained and 16% having left.

### Project Workflow
Data Cleaning and Preprocessing: The dataset was prepared for modeling through several steps:
- The data was checked for null values and duplicates, none of which were found.
- Binary features like 

Gender and OverTime were label-encoded.

Categorical features such as 

Department and JobRole were one-hot encoded.

Class imbalance was addressed by applying 

RandomOverSampler, resulting in a balanced dataset for training.

Numerical features were standardized using 

StandardScaler.

Exploratory Data Analysis (EDA): The analysis revealed several key trends correlated with attrition:


Job Role: The highest attrition counts were found among Laboratory Technicians (62), Sales Executives (57), and Research Scientists (47).


Department: The Research & Development department drives the most attrition, followed by Sales.


Work-Life Balance: Working overtime is a significant factor, with a strong correlation to attrition.


Tenure: Attrition risk is highest in the first year of employment and declines after 10 years.


Demographics: Attrition is higher among males, who constitute 63% of attrition cases. Younger employees (under 30) also show high rates of early turnover.


Predictive Modeling:

Random Forest Classifer model was selected for its interpretability in forecasting attrition risk.

The model was trained on the oversampled and scaled dataset.

The final model was exported using 

joblib for potential deployment.

Model Performance
The model achieved an overall 

accuracy of 96% on the test set. The performance for predicting which employees will leave (

Attrited class) is as follows:

Precision: 0.96 

Recall: 0.95 

F1-Score: 0.96 

Recommendations for Retention
Based on the analysis, the following retention strategies are recommended:


Enhance Onboarding: Develop mentorship programs for employees with less than 5 years of tenure to reduce first-year exits.


Focus on Career Development: Offer tailored training and promotion opportunities for high-attrition roles in R&D and Sales, such as Laboratory Technicians.


Improve Work-Life Balance: Introduce flexible work models and wellness resources to mitigate the negative effects of overtime.


Promote Diversity and Inclusion: Implement DEI training and broaden recruitment for non-STEM roles to address the high attrition rate among males.

Technologies Used
Python

Pandas

Scikit-learn

Joblib

Matplotlib & Seaborn
