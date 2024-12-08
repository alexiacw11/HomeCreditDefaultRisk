# HomeCreditDefaultRisk
Code for the Kaggle Home Credit Default Risk Competition. Created for the MSBA Practice Capstone Course.

## Business Problem
Individuals with insufficient credit histories often struggle to receive a loan from trusted lenders. Consequently, many individuals in a similar situation are taken advantage of and ultimately exploited. Home Credit aims to create a safe loaning environment for that population while being profitable for the company. The purpose of this project is to reasonably maintain inclusivity and accessibility while predicting which applicants will repay their loans. 

## Project Objectives
<ul>
<li>Deliverable of EDA findings and model predictions.
<li>GitHub repository deliverable, including code and README files. 
<li> Visually appealing slide deck that clearly conveys project findings. </ul>

## Business Value of the Solution
The advantages of predicting trusted borrowers are as follows.
<ul>
<li>The company can better determine who to accept into the program, potentially saving Home Credit substantial amounts of money.
<li> The underserved population can have a positive loan experience through curated repayment calendars.</ul>
  
## Personal Contribution to the Project
<ul>
<li>Reported EDA Including Feature Engineering 
<li>Models
  <li>Naive Bayes
  <li>LightGBM Boosted Trees
  <li>Bayesian Additive Regression Trees - BART
  <li>Random Forest
  <li>Extra Trees
  <li>Ensemble Methods
<li> Ensemble Model Slide of the Presentation </ul>

  
## Difficulties Encountered Along the Way
  1.    Missing Values: Many features contained missing values, which had the potential to reduce bias if not handled properly. Missing values represented a lack of information, errors in data entry, or genuine absences of certain attributes. Imputation techniques were carefully chosen to avoid distorting the underlying patterns in the data.
  2.    High Cardinality in Categorical Variables: Certain categorical variables, such as occupation type or income type, had unique values, ultimately increasing model complexity. High cardinality issues can lead to overfitting in models, particularly if one-hot encoding is applied without adequate dimensionality reduction.  
  3.    Imbalanced Target Variable: The target variable indicating loan default was imbalanced, with more instances of non-default than default cases. Imbalance has a tendency to bias the models toward predicting the majority class, reducing the model’s ability to identify true default risks accurately.
  4.    Inconsistent Factor Levels: Between training and test datasets, some categorical variables contained levels present in one dataset but missing in another (e.g., NAME_INCOME_TYPE). Said inconsistency complicated the application of models trained on one dataset to the other and required alignment of factor levels or handling of unknown levels.
  5.    Collinearity Among Features: Certain features, such as income and credit amounts, are likely correlated, which led to multicollinearity in linear models. Multicollinearity can inflate the variance of coefficient estimates, making the model sensitive to small changes in the data and potentially reducing interpretability.
  6.    Potential Outliers and Noise: Some numerical features contained extreme values that were potentially outliers or data entry errors. These values can distort model training, especially in distance-based or sensitive algorithms, necessitating careful inspection and possible transformation or filtering.

## Solution
<ul>
<li>All attempted models were trained on just 5% of the data
<li>The best performing was an ensemble model that achieved an AUC of 0.70311
<li>The ensemble combined predictions from: <ul>
<li>Random Forest (AUC: 0.69877)
<li>BART (AUC: 0.70113)
<li>Logistic Regression (AUC: 0.67896)
<li>Extra Trees (AUC: 0.69339)</ul>
<li>Computation Time: The ensemble model required 1.05 hours to train, balancing complexity and accuracy.
</ul>

## What I learned
<ul>
<li>The modeling process is trial and error
<li>Trying many models is crucial
<li>Including additional data does not always have a high return on investment
<li>Feature selection and engineering were key to improving model performance
<li>It is important to do robustness checks throughout the modeling process to ensure changes made are improving results
<li>The importance of being creative when interpreting business results, especially in a presentation 
</ul>

