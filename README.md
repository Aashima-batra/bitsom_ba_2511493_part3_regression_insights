# Business Problem Summary

The leadership team of a retail chain wants to understand which factors are most strongly associated with monthly sales performance across stores. The objective is to use regression analysis to identify the key drivers of sales and support decisions related to marketing investment, inventory management, customer experience, and store operations.

The findings will help leadership prioritize actions that may improve store performance and allocate resources more effectively.

---

# Dataset Description

The dataset contains monthly performance information for retail stores across different regions and store types.

Total Records: 320

Key variables included:

- Store ID
- Month
- Region
- Store Type
- Marketing Spend
- Footfall
- Average Discount Percentage
- Staff Count
- Inventory Availability Percentage
- Competitor Distance
- Holiday Flag
- Customer Rating
- Monthly Sales
- Monthly Profit

---

# Dependent Variable

The dependent variable selected for regression analysis is:

**Monthly Sales**

This variable represents the primary business outcome that leadership wants to understand and improve.

---

# Potential Independent Variables

The following variables were evaluated as potential predictors of Monthly Sales:

- Marketing Spend
- Footfall
- Average Discount Percentage
- Staff Count
- Inventory Availability Percentage
- Competitor Distance
- Holiday Flag
- Customer Rating
- Store Type

---

# Numerical Variables

The following variables were treated as numerical variables:

- Marketing Spend
- Footfall
- Average Discount Percentage
- Staff Count
- Inventory Availability Percentage
- Competitor Distance
- Customer Rating
- Monthly Sales
- Monthly Profit

---

# Categorical Variables

The following variable was identified as categorical:

- Store Type

This variable required conversion into dummy variables before it could be used in regression analysis.

---

# Variables That Need Transformation

Store Type was transformed into dummy variables to make it suitable for regression analysis.

Dummy variables created:

- Store_Airport
- Store_HighStreet
- Store_Mall

Reference Category:

- Residential

The Residential category was excluded and used as the reference category to avoid multicollinearity and the dummy variable trap.

---

# Variables Not Used

### Store ID

Store ID is a unique identifier and does not represent a business factor that directly influences sales performance. Therefore, it was excluded from the regression models.

### Month

The Month variable primarily serves as a time identifier. Since seasonality analysis was outside the scope of this project, it was not included in the final regression models.

### Monthly Profit

Monthly Profit is closely related to Monthly Sales and is considered a business outcome rather than a predictor. Therefore, it was not used as an independent variable.

---

# Initial Data Preparation Approach

Before performing regression analysis, the dataset was reviewed for:

- Missing values
- Duplicate records
- Data consistency
- Variable formatting
- Categorical variable encoding
- Outliers in key numerical variables

A prepared dataset and dummy-variable dataset were created while preserving the original data.

---

# Regression Approach

Regression analysis was performed to identify factors associated with Monthly Sales.

The analysis included:

1. Simple Regression Model using Marketing Spend
2. Simple Regression Model using Footfall
3. Multiple Regression Model using several predictors simultaneously

The purpose was to compare explanatory power and identify the most useful model for business decision-making.

---

# Simple Regression Model 1

## Dependent Variable

Monthly Sales

## Independent Variable

Marketing Spend

## Results

- R² = 0.1672
- Adjusted R² = 0.1646

## Business Interpretation

Marketing Spend showed a positive and statistically significant relationship with Monthly Sales. Stores with higher marketing investment generally generated higher sales. However, the model explained only a limited portion of sales variation.

---

# Simple Regression Model 2

## Dependent Variable

Monthly Sales

## Independent Variable

Footfall

## Results

- R² = 0.7363
- Adjusted R² = 0.7355

## Business Interpretation

Footfall demonstrated a strong positive relationship with Monthly Sales. Stores receiving more customer traffic consistently achieved higher sales performance.

---

# Multiple Regression Model

## Dependent Variable

Monthly Sales

## Independent Variables

- Marketing Spend
- Footfall
- Inventory Availability Percentage
- Customer Rating
- Store_Airport (Dummy Variable)

## Results

- R² = 0.8116
- Adjusted R² = 0.8086

The model explained approximately 81.16% of the variation in Monthly Sales and provided the strongest explanatory power among all models tested.

## Significant Variables

- Marketing Spend
- Footfall
- Inventory Availability Percentage
- Customer Rating

## Variable Requiring Caution

- Store_Airport

## Business Interpretation

The results suggest that customer traffic, marketing investment, inventory availability, and customer satisfaction are the strongest factors associated with Monthly Sales performance.

The Store_Airport dummy variable was included to represent store-type differences. However, its statistical output was not reliable enough to support strong business conclusions and should be interpreted cautiously.

---

# Dummy Variable Approach

Store Type was converted into dummy variables before regression analysis.

Dummy variables created:

- Store_Airport
- Store_HighStreet
- Store_Mall

Reference Category:

- Residential

Residential stores are represented when all Store Type dummy variables equal zero.

This approach prevents redundancy and avoids the dummy variable trap.

---

# Model Comparison Summary

| Model | R² | Business Usefulness |
|---------|---------|---------|
| Marketing Spend Model | 0.1672 | Low |
| Footfall Model | 0.7363 | High |
| Multiple Regression Model | 0.8116 | Very High |

The Multiple Regression Model provided the highest explanatory power and the strongest business value.

---

# Final Model Selected

The Multiple Regression Model was selected as the final model because:

- It achieved the highest R² value.
- It incorporates multiple business drivers simultaneously.
- It provides stronger decision-support capability than individual predictor models.
- It explains more than 81% of Monthly Sales variation.

---

# Business Recommendation

The analysis suggests that leadership should focus primarily on:

- Increasing customer footfall
- Optimizing marketing spend
- Maintaining high inventory availability
- Improving customer ratings and customer experience

These variables demonstrated the strongest and most reliable association with Monthly Sales performance.

---

# Assumptions and Limitations

Several limitations should be considered:

- Regression analysis identifies associations but does not prove causation.
- Some business factors affecting sales may not be included in the dataset.
- Economic conditions, local competition, and management practices may influence performance.
- Residual analysis indicates that additional factors may explain differences across stores.

---

# Screenshots Included

The repository includes the following screenshots:

- simple_regression_output.png
- multiple_regression_output.png
- residuals_preview.png
- model_comparison_preview.png

These screenshots provide evidence of regression outputs, model comparison results, and residual calculations used in the analysis.
