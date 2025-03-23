# Automatidata: Taxi Fare Prediction & Data Analysis

This repository contains the code and documentation for the Automatidata project, where we analyzed and built a predictive model for taxi fares using the New York City Taxi & Limousine Commission (TLC) dataset. This project encompasses exploratory data analysis (EDA), feature engineering, model building, and evaluation, along with visualizations to provide actionable insights.

## Project Overview

The goal of this project was to develop a multiple linear regression model to predict taxi fares, enabling the TLC to better understand the factors influencing fares and improve fare estimation. We also conducted a thorough EDA to uncover patterns and potential issues within the data.

## Key Objectives

* **Predict Taxi Fares:** Build a robust multiple linear regression model.
* **Identify Influencing Factors:** Determine the key variables affecting taxi fares.
* **Data Visualization:** Create insightful visualizations using Python and Tableau.
* **Data Quality Assessment:** Identify and handle outliers and missing data.
* **Feature Engineering:** Create new features to enhance model performance.
* **Business Insights:** Provide actionable recommendations to stakeholders.

## Project Structure

Automatidata/

├── 2017_Yellow_Taxi_Trip_Data.csv

├── Automatidata_project_lab.ipynb
├── PACE strategy document.docx

└── README.md


* **`2017_Yellow_Taxi_Trip_Data.csv`**: The primary dataset used for analysis.
* **`Automatidata_project_lab.ipynb`**: Jupyter Notebook containing all code, EDA, model building, and evaluation.
* **`Course 5 PACE strategy document.docx`**: Documentation of the project workflow using the PACE framework.
* **`README.md`**: This file, providing an overview and instructions for the project.

## Key Tasks Performed

1.  **Data Loading and Inspection:**
    * Loaded the dataset using pandas.
    * Inspected data types, missing values, and summary statistics.
2.  **Exploratory Data Analysis (EDA):**
    * Identified and handled outliers using box plots and statistical methods.
    * Visualized data distributions using histograms and bar charts.
    * Analyzed trip distances, fare amounts, and tip amounts.
    * Examined ridership trends by month and day.
3.  **Feature Engineering:**
    * Created new features like `duration`, `mean_distance`, `mean_duration`, `day`, `month`, and `rush_hour`.
    * Converted datetime columns to appropriate formats.
4.  **Model Building and Evaluation:**
    * Developed a multiple linear regression model using scikit-learn.
    * Evaluated model performance using R-squared, MAE, and RMSE.
    * Investigated and handled negative fare amounts, and other anomalies.
5.  **Data Visualization:**
    * Generated visualizations using matplotlib and seaborn.
    * Created a Tableau dashboard to map taxi trips by month.
6.  **Variable Investigation:**
    * Sorted and analyzed `trip_distance` and `total_amount` to look for anomalies.
7.  **Business Insights and Recommendations:**
    * Provided actionable insights based on the model and EDA.

## Dependencies

* Python (3.x)
* pandas
* numpy
* scikit-learn
* matplotlib
* seaborn
* datetime

## Getting Started

1.  **Clone the Repository:**

    ```bash
    git clone [https://github.com/yourusername/Automatidata.git](https://www.google.com/search?q=https://github.com/yourusername/Automatidata.git)
    cd Automatidata
    ```

2.  **Install Dependencies:**

    ```bash
    pip install pandas numpy scikit-learn matplotlib seaborn
    ```

3.  **Run the Jupyter Notebook:**

    * Open `Automatidata_project_lab.ipynb` in Jupyter Notebook or JupyterLab.
    * Execute the cells sequentially to reproduce the analysis and modeling.

4.  **Review Documentation:**

    * Refer to `Course 5 PACE strategy document.docx` for the project's PACE framework documentation.

## Contributing

Contributions to this project are welcome. Please feel free to submit pull requests or open issues for any improvements or bug fixes.

## Author

Charles Gregory
