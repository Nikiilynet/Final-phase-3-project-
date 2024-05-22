# SyriaTel Customer Churn Prediction

## Author
Lynette Mwiti  
Email: lynette.mwiti@student.moringaschool.com
## Project Overview
This project aims to analyze and predict customer churn for SyriaTel, a telecommunications company facing a high churn rate. The goal is to identify factors contributing to customer churn and develop a predictive model to pinpoint at-risk customers, ultimately enhancing customer retention and profitability.

## Objectives
1. Identify key factors leading to customer churn.
2. Develop a robust predictive model for customer churn.
3. Implement strategies to retain at-risk customers.

## Success Metrics
- Develop a churn prediction model with a recall score of at least 0.8.
- Identify significant features contributing to customer churn.
- Provide actionable insights and recommendations to reduce churn.
- Demonstrate the value of churn prediction models for proactive retention strategies.

## Data Understanding
### Data Source & Size
The dataset used, `customer_churn.csv`, contains 3333 records of SyriaTel customers.

### Variables Description
- `state`: Customer's state.
- `account length`: Duration of the account.
- `area code`: Area code of the phone number.
- `phone number`: Customer's phone number.
- `international plan`: Whether the customer has an international plan.
- `voice mail plan`: Whether the customer has a voicemail plan.
- `number vmail messages`: Number of voicemail messages.
- `total day minutes`: Total minutes of day calls.
- `total day calls`: Total number of day calls.
- `total day charge`: Total charge for the day calls.
- `total eve minutes`: Total minutes of evening calls.
- `total eve calls`: Total number of evening calls.
- `total eve charge`: Total charge for the evening calls.
- `total night minutes`: Total minutes of night calls.
- `total night calls`: Total number of night calls.
- `total night charge`: Total charge for the night calls.
- `total intl minutes`: Total minutes of international calls.
- `total intl calls`: Total number of international calls.
- `total intl charge`: Total charge for the international calls.
- `customer service calls`: Number of customer service calls.
- `churn`: Whether the customer churned (True/False).

## Data Preparation
### Data Cleaning
- No missing values were detected.
- No duplicate rows were found.
- The `area code` column was converted to an object type.
- The `phone number` column was dropped as it adds no value to the analysis.

### Exploratory Data Analysis (EDA)
#### Univariate Analysis
* Distribution plots were created for numeric and categorical features.
* Outliers were detected and handled appropriately.

#### Bivariate Analysis
* Relationships between variables were explored to identify potential predictors of churn.
* Boxplots and count plots were used to visualize the associations.


### Feature Engineering
- Label encoding was used to transform the `churn` feature.
- One-hot encoding was applied to categorical features.
- Numeric features were scaled using MinMaxScaler.

## Modelling
### Train-Test Split
The data was split into training and testing sets with a 75-25 ratio.

### Addressing Class Imbalance
SMOTE (Synthetic Minority Oversampling Technique) was used to balance the class distribution in the training data.

### Models Implemented
1. **Logistic Regression**
2. **Decision Tree Classifier**
3. **Random Forest Classifier**
4. **XGBoost Classifier**

### Model Evaluation
- **Metrics Used**: Recall score and ROC-AUC.
- **Results**:
  - **XGBoost Classifier**: Best performance with a recall score of 0.97 and highest AUC score.
  - **Random Forest Classifier**: Second best with a recall score of 0.96.
  - **Decision Tree Classifier**: Recall score of 0.91.
  - **Logistic Regression**: Baseline model with a recall score of 0.77.

## Recommendations
1. **State-Specific Retention Strategies**: Focus on states with higher churn rates such as Texas, New Jersey, Maryland, Miami, and New York.
2. **Targeted Promotions**: Offer discounts or promotional offers in area codes 415 and 510.
3. **Pricing Evaluation**: Adjust pricing plans for day, evening, night, and international charges.
4. **Customer Service Enhancements**: Improve customer service quality and reduce service calls.
5. **Voicemail Plan Enhancement**: Increase the value proposition of the voicemail plan to encourage adoption.

## Conclusion
The project successfully developed a predictive model for customer churn with a high recall score, exceeding the set target. The XGBoost classifier proved to be the most effective model. The recommendations provided aim to help SyriaTel reduce churn and improve customer retention.

## Repository Structure

```
├──  presentation.pdf                 <- PDF version of project presentation                     
|
├── Dsf_pt06_Phase_3_Project.ipynb    <- Narrative documentation of analysis in Jupyter Notebook
|                   
├── Customer churn.csv                 <- Dataset used in the analysis 
|
└──  README.md                        <- The README txt file for this project
     
