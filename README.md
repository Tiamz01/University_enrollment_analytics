# University_enrollment_analytics
# University Enrollment Prediction

## Overview

This project focuses on predicting student enrollment in university courses based on various factors such as course type, prerequisites, department, year, and pre/post-course scores. The dataset used for this analysis contains 1850 rows and 8 columns, with some missing values that were addressed during data preprocessing.

### Data Preprocessing

Data preprocessing is a crucial step in preparing the dataset for modeling. The following steps were performed:

1. **Handling Missing Values**: Missing values in columns like `pre_score`, `post_score`, and `pre_requirement` were addressed. Missing scores were replaced with zeros and converted to the appropriate data types, while missing prerequisites were labeled as "None."

2. **Standardization**: The `pre_score` and `post_score` columns were standardized to ensure uniform scaling.

3. **Handling Categorical Variables**: Categorical variables like `course_type`, `pre_requirement`, and `department` were one-hot encoded to convert them into numerical features.

### Exploratory Data Analysis

Several data analysis tasks were conducted:

1. **Enrollment Distribution**: The distribution of enrollment counts showed a symmetrical bimodal distribution. This distribution shape provided insights into the nature of student enrollment, with a peak indicating the highest enrollment count of approximately 261 students.

2. **Course Type Analysis**: Online courses had the highest enrollments, with 1375 students. The dataset had an imbalance in course types, with online courses dominating.

3. **Relationship Between Features**: An analysis of the relationship between course types and enrollment counts revealed that online courses had the highest enrollment rates.

### Model Building

The project utilized two regression models for prediction:

1. **Baseline Model (Linear Regression)**: A linear regression model was employed to predict enrollment counts. The dataset was split into training and testing sets, and the model was trained and evaluated.

2. **Comparison Model (Random Forest Regression)**: A more complex model, Random Forest Regression, was used for comparison. This ensemble model can capture complex non-linear relationships between features and the target variable.

### Model Evaluation

The models were evaluated based on the root mean square error (RMSE):

- Baseline Model RMSE: 35.71
- Comparison Model RMSE: 33.48

The comparison model performed slightly better with a lower RMSE, indicating a smaller residual error and a better fit.

### Prediction

Based on the comparison model's prediction, approximately 232 students are expected to enroll in the university courses.

## Conclusion

This project demonstrates the use of machine learning models to predict student enrollment in university courses based on various factors. The comparison model, a Random Forest Regression, outperformed the baseline Linear Regression model, indicating the ability to capture complex relationships in the data. Accurate enrollment predictions can assist universities in resource allocation and course planning.
