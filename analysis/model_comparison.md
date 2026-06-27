# Model Comparison

## Purpose
This document compares the simple and multiple regression models created to explain monthly store sales.

## Models Compared

| Model | Predictors | R² | Adjusted R² | RMSE | Significance | Business use |
| --- | --- | --- | --- | --- | --- | --- |
| Simple: Marketing Spend | marketing_spend | 0.167 | 0.165 | 94,846 | Significant | Limited single-factor view |
| Simple: Footfall | footfall | 0.736 | 0.735 | 53,374 | Significant | Strong demand proxy |
| Multiple Regression | numeric + region/store type dummies | 0.857 | 0.850 | 40,134 | Several significant variables | Best final model |

## Selected Final Model
The selected final model is the **Multiple Regression** model.

It was selected because it has the highest explanatory power:
- R-squared: **0.857**
- Adjusted R-squared: **0.850**
- RMSE: **40,134**

The model explains around **85.7%** of variation in monthly sales and uses both numerical drivers and categorical store characteristics.

## Why the Simple Models Were Not Enough
The marketing spend model is statistically significant, but its R-squared is only **0.167**, so it misses many important store-level factors.

The footfall model is much stronger, with R-squared **0.736**, but it still does not control for inventory availability, customer rating, region, store type, discounting, staffing, or competitor distance.

## Business Usefulness
The multiple regression model is most useful for decision-making because it helps leadership compare the effect of several variables at the same time.

Important useful variables include:
- Footfall
- Marketing spend
- Inventory availability
- Staff count
- Customer rating
- Competitor distance
- Holiday flag
- Store type and region indicators

## Limitations
- Regression shows association, not automatic causation.
- The model does not include competitor pricing, local events, product mix, or weather.
- Store-level historical patterns may affect sales but are not fully captured.
- Dummy variables must be interpreted relative to the reference groups: **East** for region and **High Street** for store type.
