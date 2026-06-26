# Model Comparison

## Overview

Three regression models were developed to understand the factors associated with Monthly Sales and to determine which model provides the most useful business insights.

---

## Model 1: Simple Regression – Marketing Spend

### Variables Used

Dependent Variable:

* Monthly Sales

Independent Variable:

* Marketing Spend

### Results

* R² = 0.1672
* Coefficient = 2.13
* P-value < 0.001

### Business Interpretation

Marketing Spend has a positive and statistically significant relationship with Monthly Sales. However, the model explains only 16.7% of the variation in sales, indicating that many other factors influence performance.

### Business Usefulness

This model provides evidence that marketing investment is associated with higher sales, but it is not sufficient as a standalone forecasting model.

### Limitations

* Low explanatory power
* Ignores other important business drivers
* Cannot fully explain sales differences between stores

---

## Model 2: Simple Regression – Footfall

### Variables Used

Dependent Variable:

* Monthly Sales

Independent Variable:

* Footfall

### Results

* R² = 0.7363
* Coefficient = 35.68
* P-value < 0.001

### Business Interpretation

Footfall has a strong positive relationship with Monthly Sales. Stores with higher customer traffic tend to generate substantially higher sales.

### Business Usefulness

This model provides strong business insight and explains approximately 73.6% of sales variation.

### Limitations

* Does not account for marketing, inventory, pricing, or regional factors
* May overestimate the importance of footfall when other variables are excluded

---

## Model 3: Multiple Regression Model

### Variables Used

Dependent Variable:

* Monthly Sales

Independent Variables:

* Marketing Spend
* Footfall
* Average Discount Percentage
* Inventory Availability Percentage
* Region_North

### Results

* R² = 0.8067
* Adjusted R² = 0.8037

Significant Variables:

* Marketing Spend
* Footfall
* Inventory Availability Percentage

Weak or Non-Significant Variables:

* Average Discount Percentage
* Region_North

### Business Interpretation

The multiple regression model explains approximately 80.7% of variation in Monthly Sales and identifies the most important business drivers while controlling for other factors.

Footfall remains the strongest predictor, followed by Marketing Spend and Inventory Availability.

### Business Usefulness

This model provides the most complete understanding of sales performance and is the most useful for decision-making.

### Limitations

* Some business factors may not be included in the dataset
* Regression identifies association rather than causation
* Certain variables were not statistically significant

---

## Overall Model Comparison

| Model               | Independent Variables                                                             | R²     | Business Usefulness |
| ------------------- | --------------------------------------------------------------------------------- | ------ | ------------------- |
| Simple Regression 1 | Marketing Spend                                                                   | 0.1672 | Low                 |
| Simple Regression 2 | Footfall                                                                          | 0.7363 | High                |
| Multiple Regression | Marketing Spend, Footfall, Avg Discount %, Inventory Availability %, Region_North | 0.8067 | Very High           |

---

## Final Model Selection

The Multiple Regression Model was selected as the final model because it achieved the highest R² value and provided the strongest overall explanation of Monthly Sales.

By incorporating multiple business drivers simultaneously, the model provides more reliable decision-support insights than either simple regression model.
