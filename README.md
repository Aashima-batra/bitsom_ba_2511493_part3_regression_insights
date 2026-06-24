# Business Problem Summary

The leadership team of a retail chain wants to understand which factors are most strongly associated with monthly sales performance across stores. The objective is to use regression analysis to identify the key drivers of sales and support decisions related to marketing investment, inventory management, staffing, discount strategy, and store operations.

The findings will help leadership prioritize actions that may improve store performance and allocate resources more effectively.

## Dataset Description

The dataset contains monthly performance information for retail stores across different regions and store types.

Total Records: 320

Key variables included:

* Store ID
* Month
* Region
* Store Type
* Marketing Spend
* Footfall
* Average Discount Percentage
* Staff Count
* Inventory Availability Percentage
* Competitor Distance
* Holiday Flag
* Customer Rating
* Monthly Sales
* Monthly Profit

## Dependent Variable

The dependent variable selected for regression analysis is:

**monthly_sales**

This variable represents the business outcome that leadership wants to understand and improve.

## Potential Independent Variables

The following variables may influence monthly sales and will be evaluated as predictors:

* marketing_spend
* footfall
* avg_discount_pct
* staff_count
* inventory_availability_pct
* competitor_distance_km
* holiday_flag
* customer_rating
* region (categorical)
* store_type (categorical)

## Numerical Variables

* marketing_spend
* footfall
* avg_discount_pct
* staff_count
* inventory_availability_pct
* competitor_distance_km
* customer_rating
* monthly_sales
* monthly_profit

## Categorical Variables

* region
* store_type

## Variables Requiring Transformation

The following categorical variables require dummy variable creation before they can be used in regression models:

* region
* store_type

Dummy variables will be created to represent these categories while avoiding the dummy variable trap by using a reference category.

## Variables That May Not Be Useful for Regression

### store_id

Store ID is a unique identifier and does not represent a business factor that directly influences sales. Therefore, it will not be used as an independent variable in the regression models.

### month

The month field is primarily a date identifier. Unless specific seasonality analysis is performed, it will not be included in the main regression models.

### monthly_profit

Monthly Profit is closely related to Monthly Sales and is considered a business outcome rather than a predictor. Therefore, it will not be used as an independent variable when predicting monthly sales.

## Initial Data Preparation Approach

Before running regression models, the dataset will be reviewed for:

* Missing values
* Duplicate records
* Data consistency
* Categorical variable encoding
* Outliers in key numerical variables

A cleaned dataset and dummy-variable dataset will be created for regression analysis while preserving the original data.
