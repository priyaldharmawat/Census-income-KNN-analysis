
# Census Income Prediction Using K-Nearest Neighbors (KNN)

## Project Overview
This project aims to predict whether an individual's income exceeds $50,000 per year using the "Census Income" dataset from the 1994 U.S. Census. The dataset consists of 48,841 records and 14 features, including demographic information such as age, education, and occupation. We use the K-Nearest Neighbors (KNN) classification algorithm to predict income levels and provide valuable insights into the factors influencing income disparity.

## Objective
- **Goal:** Predict whether an individual's income exceeds $50,000 per year.
- **Techniques Used:** 
  - K-Nearest Neighbors (KNN) Classification
  - Feature Importance using Permutation Importance
  - Data Preprocessing (handling missing values, encoding categorical variables, and scaling features)

## Data Description
The dataset used in this project is the **"adult-all.csv"**, which contains demographic information and income level for individuals. It includes the following key features:
- `age`: Age of the individual
- `education-num`: Number of years of education
- `workclass`: Type of work (e.g., government, private sector)
- `occupation`: Type of occupation (e.g., professional, sales)
- `native-country`: Country of origin
- `income`: Target variable, where income is classified as `<=50K` or `>50K`

## Steps Involved
1. **Data Preprocessing:**
   - Replacing `?` values with `NaN` and handling missing values
   - Renaming columns for better clarity
   - Splitting the data into feature variables (`X`) and target variable (`y`)
   - Encoding categorical variables using Label Encoding
   - Scaling numerical features using StandardScaler

2. **Model Building:**
   - K-Nearest Neighbors (KNN) classifier is used for predicting income levels
   - Iterating through different values of 'k' to find the optimal model
   - Achieved the highest accuracy with **k=25**, resulting in an accuracy of 83.45%

3. **Model Evaluation:**
   - Evaluated the model using a confusion matrix
   - Found that the model is effective at predicting `>50K` income but less precise for `<=50K` income
   - Investigated false positives and false negatives for model improvements

4. **Feature Importance:**
   - Used Permutation Importance to identify key features
   - Found that `education-num` is the most influential feature in predicting income levels

## Model Performance
- **Accuracy:** 83.45%
- **Confusion Matrix:**
  - True Negatives (<=50K): 9403
  - True Positives (>50K): 1918
  - False Negatives: 1396
  - False Positives: 850

## Insights
- The most significant feature for predicting income levels is `education-num`, highlighting the importance of education in income predictions.
- The KNN model provides valuable insights that could inform policies aimed at reducing income disparity based on education.
