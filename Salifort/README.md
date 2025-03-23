# Salifort Motors Employee Turnover Prediction

## Project Overview

This capstone project focuses on analyzing employee survey data from Salifort Motors, a large consulting firm, to provide data-driven suggestions to the Human Resources (HR) department regarding employee retention. The goal is to build predictive models that can identify factors influencing employee turnover and offer actionable insights.

## Description and Deliverables

Upon completion, the project will deliver:

1.  **Executive Summary:** A one-page summary for external stakeholders, outlining the project's findings and recommendations.
2.  **Code Notebook:** A comprehensive Jupyter Notebook detailing the data analysis, model building, and evaluation process.

The project requires selecting either a regression model or machine learning model to predict employee turnover. The deliverables will include model evaluation, data visualizations, ethical considerations, and troubleshooting resources.

## Company Background

Salifort Motors is a large consulting firm concerned about high employee turnover rates. The HR department aims to improve employee satisfaction and retention by analyzing employee survey data.

## Business Case

The HR department seeks to understand the factors driving employee turnover to develop effective retention strategies. Predicting which employees are likely to leave can help identify and address these factors, reducing the costs associated with hiring and training new employees.

## Data

The dataset contains 15,000 rows and 10 columns, including:

* `satisfaction_level`: Employee-reported job satisfaction level [0–1]
* `last_evaluation`: Score of employee's last performance review [0–1]
* `number_project`: Number of projects employee contributes to
* `average_monthly_hours`: Average number of hours employee worked per month
* `time_spend_company`: How long the employee has been with the company (years)
* `Work_accident`: Whether or not the employee experienced an accident while at work
* `left`: Whether or not the employee left the company
* `promotion_last_5years`: Whether or not the employee was promoted in the last 5 years
* `Department`: The employee's department
* `salary`: The employee's salary (U.S. dollars)

## Methodology

This project follows the PACE (Plan, Analyze, Construct, Evaluate, Execute) methodology:

### Plan

* **Stakeholders:** Senior Leadership Team, HR Department, Department Managers, Employees.
* **Goals:** Predict employee turnover, identify contributing factors, and provide retention recommendations.
* **Initial Observations:** Analysis of data distributions, correlations, and potential issues (missing values, outliers).
* **Resources:** Python libraries (pandas, NumPy, scikit-learn, matplotlib, seaborn, XGBoost), online documentation, tutorials.
* **Ethical Considerations:** Data privacy, bias awareness, transparency, responsible interpretation.

### Analyze

* **EDA (Exploratory Data Analysis):** Analyzing relationships between variables, data distributions, and identifying patterns.
* **Data Cleaning:** Handling missing values, duplicates, and outliers.
* **Feature Engineering:** Transforming and creating new features to improve model performance.
* **Visualization:** Creating visualizations to understand data patterns and relationships.
* **Observations:**
    * Strong negative correlation between satisfaction and turnover.
    * Higher average monthly hours and lower salaries correlate with higher turnover.
    * Imbalanced target variable ('left').
    * Skewed satisfaction levels.
    * Outliers in tenure, monthly hours, and number of projects.
* **Transformations:** Renaming columns, dropping duplicates.
* **Resources:** Python libraries, documentation, online tutorials, YouTube.
* **Ethical Considerations:** Data privacy, bias awareness, transparency, data accuracy.
* **Additional EDA:**
    * Analysis of employee turnover rates before and after removing duplicates.
    * Correlation heatmap to visualize relationships between numerical features.
    * Distribution plots for 'left' (turnover), satisfaction levels, and other key variables.
    * Count plots and box plots to examine relationships between categorical and numerical variables with turnover.
    * Pair plot to visualize pairwise relationships between numerical features and turnover.
    * Statistical analysis to quantify relationships (e.g., correlation coefficients, chi-squared tests).
* **Insights from Data Analysis:**
    * **Correlation Analysis:**
        * Strong negative correlation between satisfaction and turnover (-0.35).
        * Positive correlation between average monthly hours and turnover (0.07).
        * Positive correlation between tenure and turnover (0.17).
        * Negative correlation between work accidents and turnover (-0.12).
        * High correlation between number of projects and average monthly hours.
        * Positive correlation between last evaluation and number of projects.
    * **Distribution of 'left' (Turnover):** Imbalanced data with more employees staying (10,000) than leaving (1,991).
    * **Distribution of Satisfaction Levels:** Mean satisfaction around 0.63, skewed towards low levels.
    * **Department vs. Left:** Sales, technical, and support have high turnover; management has low turnover.
    * **Salary vs. Left:** Low salaries correlate with high turnover; high salaries with low turnover.
    * **Tenure vs. Left:** Employees who left had slightly higher average tenure.
    * **Average Monthly Hours vs. Left:** Employees who left worked slightly longer hours.
    * **Number of Projects vs. Left:** Employees who left had slightly more projects.
    * **Overall Insights:** Low satisfaction, low salary, and high workload are key turnover drivers.

### Construct

* **Model Selection:** Logistic Regression, Decision Tree, XGBoost, Random Forest, SVM.
* **Model Training:** Training models on the prepared data.
* **Feature Selection:** Using all available features, one-hot encoding categorical variables.
* **Hyperparameter Tuning:** RandomizedSearchCV for XGBoost.
* **Model Assumptions:**
    * Logistic Regression: Outcome variable categorical, independent observations, no severe multicollinearity (partially met), no extreme outliers, linear relationship between X and logit (not explicitly checked), sufficient sample size (assumed).
    * **Findings:**
        * XGBoost (tuned) and Random Forest showed best performance.
        * Logistic Regression had poor performance, likely due to multicollinearity and class imbalance.
        * XGBoost Identified satisfaction, number of projects, and tenure as the most important features.

### Evaluate

* **Model Evaluation:** Accuracy, precision, recall, F1-score, AUC-ROC, Cohen's Kappa.
* **Interpretation:** XGBoost (tuned) had the best performance.
* **Validation:** Ensuring model robustness and generalizability.
* **Results:**
    * XGBoost (tuned) had the highest AUC-ROC (0.9829), Cohen's Kappa (0.9258), and balanced accuracy (0.9481).
    * Logistic Regression had the lowest performance, with a low Cohen's Kappa (0.1979).

### Execute

* **Interpretation:**
    * XGBoost (tuned) is the preferred model for deployment.
    * Logistic Regression is unreliable due to class imbalance and multicollinearity.
    * Hyperparameter tuning is crucial for model performance.
* **Actionable Steps:**
    * Implement strategies to improve employee satisfaction.
    * Review and adjust salary structures.
    * Manage employee workloads to prevent burnout.
    * Develop targeted retention plans for high-turnover departments.
    * Investigate the causes of long tenured employees leaving.
    * Address multicollinearity and class imbalance issues in future modeling.
* **A/B Testing:**
    * Simulated A/B tests to evaluate HR interventions (mentorship, flexible hours, salary, training).
    * Demonstrated significant impact of mentorship, flexible hours, and training.
    * Highlighted the importance of real-world A/B testing.
* **Ethical Considerations:**
    * Ensure data privacy and prevent discriminatory outcomes.
    * Communicate model usage transparently to employees.
    * Continual evaluation of the model's generalizability and external validation.
* **Model Results Summary:**
    * XGBoost (tuned) is the most reliable model for predicting employee turnover.
    * Focus on key predictors (satisfaction, workload, tenure).
    * Implement targeted retention strategies and HR interventions.
    * Enhance data collection and monitoring.
    * Maintain ethical considerations and transparency.
* **Recommendations:**
    * Implement XGBoost model in HR.
    * Focus on key predictors of turnover.
    * Develop targeted retention strategies.
    * Use A/B testing for HR programs.
    * Enhance data collection and monitoring.
    * Prioritize ethical considerations and transparency.
* **Next Steps:**
    * Calculate costs and benefits of retention strategies.
    * Run a pilot program.
    * Build an HR dashboard.
    * Investigate department and job issues.
    * Keep the model updated.
    * Gather employee feedback.
    * Conduct real-world A/B tests.

## Files

* `PACE_Strategy_Document.md`: Contains the answers to
