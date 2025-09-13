# What drives the price of a car?

## Business Understanding

* Our goal is to develop a supervised regression model to predict the price of used cars. 
* The target variable is 'price', and the features are the car's attributes like 'year', 'manufacturer', 'model', etc. 
* By analyzing the model, we can identify which features most significantly influence the price. 
* This will help a used car dealership understand consumer values, optimize their inventory, and refine their pricing strategies.

## Data Understanding

To understand the dataset, I would take the following steps:
1. **Load the data**: Read the `vehicles.csv` file into a pandas DataFrame.
2. **Initial Exploration**: Examine the first few rows, column names, and data types.
3. **Descriptive Statistics**: Generate summary statistics for numerical columns to understand their distribution (e.g., mean, median, min, max).
4. **Missing Values**: Check for missing values in each column to identify data quality issues.
5. **Target Variable Analysis**: Analyze the distribution of the 'price' column to spot outliers or skewness.
6. **Feature Analysis**:
    - For categorical features, I'll examine the unique values and their frequencies.
    - For numerical features, I'll look at their distributions using histograms.
7. **Correlation Analysis**: Investigate relationships between features and the target variable, 'price'.

## Modeling
For modeling, I would use the below models to predict the price of used cars with RMSE and R2 as evaluation metrics:
1. Linear Regression
2. Lasso Regression
3. Polynomial Regression
4. Random Forest Regression

## Evaluation
## Model Performance Comparison

| Model                 | RMSE        | R2       |
|-----------------------|-------------|----------|
| Linear Regression     | 9023.950148 | 0.622316 |
| Lasso Regression      | 9023.936045 | 0.622317 |
| Polynomial Regression | 8361.569739 | 0.675727 |
| Random Forest         | 6439.219794 | 0.807690 |

1. check this link for more details: https://github.com/licyambrose/carpriceproject/blob/main/assignment_2_carprice_prediction.ipynb
2. We found that the Random Forest Regression model performed the best with an RMSE of 6439.219794 and an R2 score of 0.807690 on the test set.
3. Bar plot showing feature importance from the Random Forest model:

## Deployment
## Report for Used Car Dealership

### Key Findings on Used Car Pricing

Our analysis, using a Random Forest model that explains approximately 72% of the variance in car prices, has identified several key factors that significantly drive the price of a used car.

**The Most Important Factors:**

1.  **Age and Odometer Reading**: Unsurprisingly, `age` and `odometer` are the two most critical factors. Newer cars and those with lower mileage command significantly higher prices. The model shows that for every year older a car is, the price drops substantially.

2.  **Manufacturer**: The brand of the car plays a huge role. Luxury brands like `mercedes-benz`, `porsche`, and `audi` are associated with much higher prices, while budget-friendly brands like `hyundai` and `kia` have a negative impact on price compared to the average.

3.  **Drivetrain (4WD)**: Having `4wd` is a strong positive feature, indicating that customers are willing to pay a premium for the added capability, especially in certain regions or for specific vehicle types like SUVs and trucks.

4.  **Cylinders**: The number of `cylinders` is also a significant price driver. Vehicles with more cylinders (e.g., 8-cylinder engines) are generally more expensive.

**Actionable Recommendations for the Dealership:**

*   **Inventory Strategy**:
    *   **Prioritize Low-Age, Low-Mileage Vehicles**: These are your most valuable assets. Focus acquisition efforts on well-maintained, newer models.
    *   **Stock High-Value Brands**: Investing in an inventory of sought-after luxury and reliable brands (like Ford, Chevrolet, and Ram, which also show positive price influence) can lead to higher profit margins.
    *   **Leverage 4WD**: Actively stock and market 4WD vehicles, especially if your dealership is in an area with adverse weather conditions. Highlight this feature in your listings.

*   **Pricing Strategy**:
    *   Use the key drivers (`age`, `odometer`, `manufacturer`, `4wd`) as the primary factors in your pricing model.
    *   For vehicles that are not selling, our data suggests that `age` and `odometer` are the most likely reasons. Consider price adjustments on older, high-mileage cars more aggressively.

*   **Marketing**:
    *   In your marketing materials, emphasize the key features that drive value. For example, "Low Mileage 2022 Ford F-150 4x4" is a title that hits on three of the most important price drivers.

By aligning your inventory, pricing, and marketing strategies with these data-driven insights, you can better meet customer demand and maximize profitability.