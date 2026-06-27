# Residual Analysis

## Purpose
Residual analysis compares actual monthly sales with predicted monthly sales from the final multiple regression model.

Residual = Actual Monthly Sales - Predicted Monthly Sales

A positive residual means the model under-predicted sales.  
A negative residual means the model over-predicted sales.

## Final Model Residual Summary
- Number of records analyzed: **320**
- Final model R-squared: **0.857**
- Final model adjusted R-squared: **0.850**
- RMSE: **40,134**

## Top Positive Residuals
These stores performed better than the model expected.

| Store ID | Month | Actual Sales | Predicted Sales | Residual | Region | Store Type |
| --- | --- | --- | --- | --- | --- | --- |
| STR-1058 | 2025-02-01 | 870,937 | 759,920 | 111,017 | East | High Street |
| STR-1028 | 2025-04-01 | 713,611 | 610,532 | 103,079 | East | Mall |
| STR-1073 | 2025-03-01 | 813,317 | 721,416 | 91,901 | East | Residential |
| STR-1051 | 2025-02-01 | 787,716 | 701,381 | 86,334 | East | Airport |
| STR-1026 | 2025-04-01 | 625,514 | 540,235 | 85,279 | East | Mall |

## Top Negative Residuals
These stores performed worse than the model expected.

| Store ID | Month | Actual Sales | Predicted Sales | Residual | Region | Store Type |
| --- | --- | --- | --- | --- | --- | --- |
| STR-1023 | 2025-02-01 | 627,172 | 764,039 | -136,867 | South | Mall |
| STR-1017 | 2025-03-01 | 685,379 | 805,280 | -119,901 | West | High Street |
| STR-1012 | 2025-01-01 | 595,468 | 709,914 | -114,446 | West | Residential |
| STR-1007 | 2025-02-01 | 800,452 | 912,345 | -111,893 | West | Mall |
| STR-1060 | 2025-01-01 | 721,079 | 808,022 | -86,942 | West | Mall |

## Business Interpretation
Large positive residuals may indicate stores that benefited from local factors not captured in the dataset, such as better visual merchandising, local promotions, product availability, or store manager effectiveness.

Large negative residuals may indicate operational issues, local competition, stock-outs, poor customer experience, or weaker execution compared with similar stores.

## Over-Prediction and Under-Prediction Risk
The model may under-predict high-performing stores that have strong local execution or unmeasured customer demand. It may over-predict stores where measured drivers look strong but local conditions reduce actual sales.

## Limitation
Residuals should be reviewed by business teams before taking action. A large residual is a signal for investigation, not final proof of success or failure.
