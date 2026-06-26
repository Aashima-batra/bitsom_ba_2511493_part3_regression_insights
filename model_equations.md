## Dummy Variable Approach

The categorical variable store_type was converted into dummy variables before running regression.

The original categories were:

- Residential
- Airport
- High Street
- Mall

Residential was selected as the reference category.

The following dummy variables were created:

- Dummy_Airport
- Dummy_Highstreet
- Dummy_Mall

A value of 1 indicates that the store belongs to that category, while 0 indicates otherwise.

Residential stores are represented when all dummy variables equal 0.

This approach avoids the dummy variable trap and allows regression coefficients to be interpreted relative to Residential stores.



## Simple Regression Model 1

### Model

Monthly Sales = 560777.35 + 2.13 × Marketing Spend

### Results

* R² = 0.1672
* Marketing Spend Coefficient = 2.13
* P-value = 2.48E-14

### Business Interpretation

Marketing Spend has a positive and statistically significant relationship with Monthly Sales. On average, every additional unit of marketing spend is associated with an increase of approximately 2.13 units in monthly sales.

Although significant, this model explains only 16.7% of sales variation, indicating that additional business factors should be included in a more comprehensive model.



## Simple Regression Model 2

### Model

Monthly Sales = 446410.58 + 35.68 × Footfall

### Results

* R² = 0.7363
* Footfall Coefficient = 35.68
* P-value = 4.75E-94

### Business Interpretation

Footfall has a strong positive and statistically significant relationship with Monthly Sales. Each additional customer visit is associated with approximately 35.68 units of additional monthly sales.

This model explains approximately 73.6% of the variation in sales, making Footfall a substantially stronger predictor than Marketing Spend.



# Multiple Regression Model

## Variables Used

### Dependent Variable
- Monthly Sales

### Independent Variables
- Marketing Spend
- Footfall
- Inventory Availability Percentage
- Customer Rating
- Store_Airport (Dummy Variable)

---

## Regression Results

### Model Performance

- R² = 0.8116
- Adjusted R² = 0.8086
- Observations = 320
- Significance F = 1.7562E-111

The model explains approximately 81.16% of the variation in Monthly Sales, indicating strong explanatory power.

---

## Coefficient Interpretation

### Intercept

Coefficient = 90,431.39

The intercept represents the estimated Monthly Sales when all predictor variables are zero. While this scenario may not be realistic in practice, it provides the baseline value for the regression equation.

### Marketing Spend

Coefficient = 1.203

P-value = 7.83E-18

Marketing Spend has a positive and statistically significant relationship with Monthly Sales. Holding other variables constant, an increase of one unit in Marketing Spend is associated with an increase of approximately 1.20 units in Monthly Sales.

### Footfall

Coefficient = 33.635

P-value = 3.86E-101

Footfall is the strongest predictor in the model. Holding other variables constant, each additional customer visit is associated with approximately 33.64 additional units of Monthly Sales.

### Inventory Availability Percentage

Coefficient = 2951.73

P-value = 1.66E-09

Inventory Availability has a positive and statistically significant relationship with Monthly Sales. Stores with higher inventory availability tend to generate higher sales.

### Customer Rating

Coefficient = 10,735.47

P-value = 0.0008

Customer Rating has a positive and statistically significant relationship with Monthly Sales. Stores receiving better customer ratings tend to achieve higher sales performance.

### Store_Airport (Dummy Variable)

Coefficient = 0

P-value = #NUM!

The Store_Airport dummy variable produced invalid statistical results. This suggests that the variable may contain insufficient variation or a data preparation issue. Therefore, it should not be interpreted for business decision-making.

---

## Direction of Relationships

| Variable | Relationship with Monthly Sales |
|-----------|-----------|
| Marketing Spend | Positive |
| Footfall | Positive |
| Inventory Availability Percentage | Positive |
| Customer Rating | Positive |
| Store_Airport | Not Interpretable |

---

## Business Interpretation

The analysis suggests that Footfall, Customer Rating, Inventory Availability, and Marketing Spend are the most important factors associated with Monthly Sales.

Footfall has the strongest impact on sales performance, indicating that initiatives aimed at increasing customer traffic may generate the greatest business benefit.

Inventory management and customer experience also appear to be important drivers of sales performance.

The Store_Airport dummy variable produced invalid statistics and should not be used for business conclusions.