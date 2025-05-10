# Predicting Used Car Prices in the US Market

This repository contains the code and resources for a machine learning case study focused on predicting used car prices in the United States. The project was undertaken to provide data-driven insights and a predictive model for Jason Motors Group (JMG), an Australian used car dealership planning expansion into the US market.

## Project Overview

The primary objective of this project was to develop a supervised machine learning model capable of accurately estimating the selling prices of used cars in the US market. This model aims to assist JMG with strategic decision-making regarding inventory management, pricing strategies, and overall profitability.

The project involved:
* Comprehensive data acquisition from Craigslist.
* Extensive data preprocessing to handle missing values, outliers, and feature engineering.
* In-depth Exploratory Data Analysis (EDA) to uncover key market insights.
* Development and optimisation of a Random Forest Regressor model.
* Evaluation of model performance using relevant metrics.
* Formulation of actionable business recommendations for JMG.

## Key Features

* **Data Preprocessing:** Scripts for cleaning, transforming, and preparing raw used car data for machine learning.
* **Exploratory Data Analysis (EDA):** Visualisations and code to understand market trends, price determinants, and feature relationships.
* **Machine Learning Model:** Implementation of a Random Forest Regressor for price prediction, including hyperparameter tuning using GridSearchCV.
* **Model Evaluation:** Code to assess model performance using R-squared and Mean Squared Error (MSE).
* **Insights & Recommendations:** Derivation of key business insights and actionable recommendations based on the model and analysis.

## Dataset

The dataset used in this project (`JMG_data.csv`) was sourced from Craigslist listings for used cars in the US. It includes various attributes such as:
* `make`, `model`, `vehicle_type`, `size`, `condition`
* `odometer`, `year` (build year)
* `fuel_type`, `cylinders`, `transmission`, `paint_color`, `title_status`, `state`
* `price` (target variable)

## Methodology

1.  **Data Loading & Initial Inspection:** Loading the `JMG_data.csv` into a Pandas DataFrame and performing initial checks (`.head()`, `.info()`, `.describe()`).
2.  **Data Cleaning & Preprocessing:**
    * Handling missing values through imputation (mode for categorical, median for numerical).
    * Outlier treatment using the Interquartile Range (IQR) method for 'price', 'odometer', and 'year'.
    * Feature engineering: Creating an 'Age' feature from 'year'.
    * Data transformation: Log transforming 'odometer' for normalisation.
    * Categorical encoding: One-hot encoding for relevant categorical features.
3.  **Exploratory Data Analysis (EDA):** Visualising data distributions, relationships between features, and the impact of various attributes on car prices (e.g., popularity by make/model, price vs. odometer/age, price by vehicle type/condition).
4.  **Model Development:**
    * Splitting data into training and testing sets (80/20 split).
    * Implementing a baseline Linear Regression model.
    * Implementing a Random Forest Regressor for superior performance.
5.  **Hyperparameter Tuning:** Utilising `GridSearchCV` to optimise the Random Forest model's hyperparameters (e.g., `n_estimators`, `max_features`, `min_samples_leaf`).
6.  **Model Evaluation:** Assessing the performance of both models using R-squared and Mean Squared Error (MSE) metrics to determine predictive accuracy.

## Results and Performance

The optimised Random Forest Regressor demonstrated strong predictive capabilities:
* **R-squared:** 0.787 (explains approximately 79% of the variance in used car prices).
* **Mean Squared Error (MSE):** 29,880,022 (indicating high accuracy in price predictions).

This performance significantly outperforms the baseline Linear Regression model (R-squared: 0.448, MSE: 77,000,000).

## Repository Structure

```
.
├── JMG_data.csv                  # The dataset used for the project
├── MIS710A1_Kush_223581218.ipynb # Jupyter Notebook containing the project code
├── README.md                     # This README file
└── (optional) images/            # Directory for charts/visualisations used in the notebook or blog
```

## How to Use

To run this project locally:

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    cd your-repo-name
    ```
2.  **Install Dependencies:**
    It is recommended to use a virtual environment.
    ```bash
    pip install pandas numpy scikit-learn matplotlib seaborn
    ```
    (Note: Specific versions might be required as per the notebook's environment.)
3.  **Open and Run the Notebook:**
    Open the `MIS710A1_Kush_223581218.ipynb` file using Jupyter Notebook or JupyterLab and run the cells sequentially.

## Related Resources

* **Project Report (PDF):** [Link to your PDF report here]
* **Blog Post (Case Study):** [Link to your blog post here]

## Acknowledgements

This project was completed as part of a Machine Learning in Business course (MIS710) at Deakin University.

## Contact

For any questions or further information, please contact [Your Name/Email/LinkedIn].
