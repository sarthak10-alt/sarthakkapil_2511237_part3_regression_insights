# sarthakkapil_2511237_part3_regression_insights
# Retail Monthly Sales Regression Analysis

## Business Problem Summary
A retail chain wants to understand which factors are most strongly associated with monthly sales across stores. Leadership is considering actions such as increasing marketing spend, improving inventory availability, changing discounting strategy, reallocating staff, and prioritizing certain store types or regions.

The goal of this project is to use regression analysis to identify key sales drivers and provide a business recommendation.

## Dataset Description
The dataset used is `business_regression_data.xlsx`.

It contains **320 records** across **80 stores**, covering monthly store performance between **2025-01-01** and **2025-04-01**.

## Dependent Variable
The dependent variable is:

- `monthly_sales`

## Independent Variables Considered
Numerical independent variables:
- `marketing_spend`
- `footfall`
- `avg_discount_pct`
- `staff_count`
- `inventory_availability_pct`
- `competitor_distance_km`
- `holiday_flag`
- `customer_rating`

Categorical variables:
- `region`
- `store_type`

## Dataset Preparation
The dataset was reviewed for missing values, categorical variables, and variables useful for regression.

Missing values found:
| Column | Missing Count |
| --- | --- |
| competitor_distance_km | 6 |
| customer_rating | 8 |

Missing numerical values were handled using median imputation:
- `competitor_distance_km` median used: **3.365**
- `customer_rating` median used: **3.9**

No rows were removed.

## Regression Approach
The following models were created:
1. Simple regression using `marketing_spend`
2. Simple regression using `footfall`
3. Multiple regression using numerical predictors and dummy variables

## Dummy Variable Approach
Dummy variables were created for:
- `region`
- `store_type`

Reference categories:
- Region: **East**
- Store type: **High Street**

One category was excluded from each categorical variable to avoid redundancy.

## Model Comparison Summary

| Model | Predictors | R² | Adjusted R² | RMSE | Significance | Business use |
| --- | --- | --- | --- | --- | --- | --- |
| Simple: Marketing Spend | marketing_spend | 0.167 | 0.165 | 94,846 | Significant | Limited single-factor view |
| Simple: Footfall | footfall | 0.736 | 0.735 | 53,374 | Significant | Strong demand proxy |
| Multiple Regression | numeric + region/store type dummies | 0.857 | 0.850 | 40,134 | Several significant variables | Best final model |

## Final Model Selected
The final selected model is the **Multiple Regression** model because it has the highest R-squared and adjusted R-squared and gives a broader business view.

## Business Recommendation
The strongest business recommendation is to focus on:
- Growing footfall
- Improving inventory availability
- Supporting marketing with operational readiness
- Allocating staff based on store traffic
- Improving customer rating
- Avoiding blind discounting

## Assumptions and Limitations
- Regression shows association, not causation.
- The model does not include all possible external factors.
- Missing values were handled using median imputation.
- Results should be used with business judgment.
- Dummy variable results are relative to the selected reference categories.

## Screenshots Included
The `screenshots/` folder includes:
- `simple_regression_output.png`
- `multiple_regression_output.png`
- `residuals_preview.png`
- `model_comparison_preview.png`

## Files Included
- `data/business_regression_data.xlsx`
- `analysis/regression_workbook.xlsx`
- `analysis/model_comparison.md`
- `analysis/residual_analysis.md`
- `outputs/regression_summary.xlsx`
- `outputs/model_equations.md`
- `outputs/final_recommendation.md`
- `screenshots/`
- `README.md`
