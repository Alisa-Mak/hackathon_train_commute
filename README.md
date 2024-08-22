# Hackathon - Shinkansen Travel Experience

## Achievements:

Participating in the MIT Professional Education Applied Data Science **Hackathon** competition was an incredible experience, where I **competed alongside industry experts** and secured **5th place**. This achievement allowed me to apply the extensive knowledge I gained from the **MIT Data Science** program, demonstrating both my skills and dedication to the field of data science.

![image](https://github.com/user-attachments/assets/97fcffc2-192e-438f-85e6-146e3ed592bc)

## Background:
This problem statement is based on the Shinkansen **Bullet Train in Japan**, and passengers’ experience with that mode of travel. This machine-learning exercise **aims to determine** the relative importance of each parameter with regard to their contribution to the passengers’ **overall travel experience**. The dataset contains a random sample of individuals who traveled on this train. The on-time performance of the trains along with passenger information is published in a file named ‘Traveldata_train.csv’.  These passengers were later asked to provide their feedback on various parameters related to the travel along with their overall experience. These collected details are made available in the survey report labeled ‘Surveydata_train.csv’.

In the survey, each passenger was explicitly asked whether they were satisfied with their overall travel experience or not, and that is captured in the data of the survey report under the variable labeled ‘Overall_Experience’. 

The objective of this problem is to **understand which parameters play an important role** in swaying passenger feedback towards a positive scale. You are provided test data containing the travel data and the survey data of passengers. Both the test data and the train data are collected at the same time and belong to the same population.

## Goal:
The goal of the problem is to predict whether a passenger was satisfied or not considering his/her overall experience of traveling on the Shinkansen Bullet Train.

## Dataset: 

The problem consists of 2 separate datasets: Travel data & Survey data. Travel data has information related to passengers and attributes related to the Shinkansen train, in which they traveled. The survey data is aggregated data of surveys indicating the post-service experience. You are expected to treat both these datasets as raw data and perform any necessary data cleaning/validation steps as required.

The data has been split into two groups and provided in the Dataset folder. The folder contains both train and test data separately.

Train_Data
Test_Data

## Target Variable: 
Overall_Experience (1 represents ‘satisfied’, and 0 represents ‘not satisfied’)

Here's a summarized and polished version for your README:

### Strategy Overview:

1. **Understanding the Data (EDA)**:
   - Conducted thorough Exploratory Data Analysis to gain insights into the dataset.

2. **Handling Missing Values**:
   - Removed rows with less than 1% missing values.
   - For continuous variables with more than 1% missing values, used KNNImputer.
   - Imputed categorical variables with the mode.

3. **Feature Engineering**:
   - A crucial part of the process, focusing on creating new features that capture the essence of the data.
   - Generated features such as `Total_Delay`, `Average_Delay`, `Overall_Rating`, and interaction terms.
   - Used these engineered features to improve model performance.

4. **Normalization and Handling Outliers**:
   - Normalized continuous features and handled outliers to ensure robust model performance.

5. **Feature Selection**:
   - Selected the most relevant features using techniques like Chi-square tests.

6. **Model Training**:
   - Decision Trees were identified as suitable for this classification problem.
   - Tried various models and compared their performance:

| Model                           | Accuracy  |
|---------------------------------|-----------|
| Decision Tree                   | 0.930000  |
| Bagging Decision Tree Classifier| 0.947700  |
| Bagging XGBoost Classifier      | 0.952300  |
| Bagging Random Forest Classifier| 0.951900  |
| AdaBoost                        | 0.893500  |
| Gradient Boosting               | 0.919400  |
| XGBoost                         | 0.954400  |
| Ensemble                        | 0.956200  |
| CatBoost                        | 0.960000  |
| CatBoost Calibrated             | 0.954400  |

### Steps to Improve Model Performance:
- Fine-tuning hyperparameters using GridSearch and RandomSearch.
- Calibration, cross-validation, and regularization.
- Adjusting learning rates for better convergence.

### Data Quality Improvements:
- Handling missing values and outliers.
- Filtering noise and normalizing data.

### Lessons Learned:
- The performance of a model heavily depends on the **quality of the data**. Ensuring high-quality data is a crucial step for achieving accurate and reliable results.
