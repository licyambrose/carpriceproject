# What drives the price of a car?

## Business Understanding

*   Formulate the task as a supervised regression problem to predict used car prices.
*   Use car features (e.g., make, model, year, mileage, condition) as predictor variables.
*   Apply feature engineering and exploratory data analysis to identify influential predictors.
*   Clean and transform the dataset to ensure data quality and consistency.
*   Train and evaluate machine learning models to quantify feature importance.
*   Extract actionable insights to inform pricing strategies for used car dealerships.

## Data Understanding

*   Explore the dataset to understand available features (e.g., make, model, year, mileage, condition, price). Assess data quality, missing values, and feature distributions.

Here are steps to understand the dataset and identify quality issues:

1.  **Load the data:** Use pandas to load the `vehicles.csv` dataset into a DataFrame.
2.  **Inspect the data:**
    *   Use `.head()` to view the first few rows and understand the columns.
    *   Use `.info()` to check data types and non-null counts.
    *   Use `.describe()` to get summary statistics for numerical columns.
3.  **Check for missing values:** Use `.isnull().sum()` to identify columns with missing values and the number of missing entries.
4.  **Explore categorical variables:**
    *   Use `.value_counts()` to understand the distribution of unique values in categorical columns.
    *   Look for inconsistencies or errors in the categories.
5.  **Explore numerical variables:**
    *   Create histograms and box plots to visualize distributions and outliers.
    *   Check for unusual or impossible values (e.g., negative mileage).
6.  **Identify potential data quality issues:**
    *   Inconsistent formatting.
    *   Outliers.
    *   Incorrect data types.
    *   Duplicate entries.
7.  **Consider the relevance of each feature** to the business understanding and how it might influence used car prices.