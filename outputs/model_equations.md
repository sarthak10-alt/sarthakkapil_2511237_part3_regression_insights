# Model Equations

## Dependent Variable
The dependent variable for all models is:

**monthly_sales**

## Reference Categories for Dummy Variables
For categorical variables, the following reference categories were used:
- Region reference category: **East**
- Store type reference category: **High Street**

These categories were excluded from dummy variables to avoid redundancy.

## Simple Regression Equation 1
**Predictor:** marketing_spend

```text
monthly_sales = 560,777.35 + 2.13 × marketing_spend
```

Business meaning:
For every 1 unit increase in marketing spend, monthly sales are associated with an increase of approximately **2.13**.

## Simple Regression Equation 2
**Predictor:** footfall

```text
monthly_sales = 446,410.58 + 35.68 × footfall
```

Business meaning:
For each additional customer footfall unit, monthly sales are associated with an increase of approximately **35.68**.

## Multiple Regression Equation

```text
monthly_sales = 61,843.31 + 1.21 × marketing_spend + 27.34 × footfall - 41,243.15 × avg_discount_pct + 3,508.40 × staff_count + 3,062.21 × inventory_availability_pct - 3,438.11 × competitor_distance_km + 15,157.29 × holiday_flag + 12,509.46 × customer_rating + 9,948.71 × region_North + 21,089.57 × region_South + 25,291.42 × region_West + 24,475.84 × store_type_Airport + 12,613.59 × store_type_Mall - 20,219.26 × store_type_Residential
```

## Coefficient Interpretation
The multiple regression coefficients are interpreted while holding other variables constant.

Important interpretations:
- **Footfall:** Higher store visits are strongly associated with higher monthly sales.
- **Marketing spend:** Higher marketing spend is associated with higher monthly sales.
- **Inventory availability:** Better inventory availability is associated with higher sales.
- **Customer rating:** Better customer rating is associated with higher monthly sales.
- **Competitor distance:** The negative coefficient means stores farther from competitors showed lower sales in this dataset, which may reflect that stronger commercial areas have closer competitors.
- **Holiday flag:** Holiday months are associated with higher sales.
- **Store type dummies:** Airport and Mall stores are interpreted relative to High Street stores.
- **Region dummies:** North, South, and West are interpreted relative to East.

## Final Model Selected
The final selected model is the **Multiple Regression** model because it has the strongest explanatory power and includes both operational and store-characteristic variables.

## Reason for Selecting the Final Model
The multiple regression model has:
- R-squared: **0.857**
- Adjusted R-squared: **0.850**
- RMSE: **40,134**

It is more useful than simple regression because it controls for multiple business drivers at the same time.
