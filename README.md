<h1 align="center">Capstone Project Walmart</h1> 

![graph1](./Images/walmart1.png)

**Author: Chris Freyre**

## Project Overview & Business Problem

In this project I gathered csv file from kaggle only for educational purpose. Walmart has been running out of stock during busy periods recently and are looking for a way to predict future sales in order to maintain appropriate levels of stock.

## Data Understanding

Walmart.csv file contains 6435 rows and 8 columns for the period of 2010-2012. Analysing the data we can say that it has 45 stores, a price in relation to weekly sales, holiday days, temperature, fuel price, Consumer price index (CPI) and unemployment. 

Columns:

  * Store         45 number of stores
  * Date          day-mont-year of sale
  * Weekly_Sales  sales in given stores
  * Holiday_Flag  0 for no holyday day | 1 for holiday day
  * Temperature   ℉ in days of sales
  * Fuel_price    Fuel cost on day sales
  * CPI           Consumer price index
  * Unemployment  Unemplyment rate
  
  
![graph1](./Images/hist_gram.png)  


## Data Cleaning
  
* I started checking for missing and unique values in each column. 
* Proceded to convert date into weeks, months and year.
* Created a segmentation of the data by Quarters for better understanding.
* Found in weekly sales, temperature and unemployment outliers, that performinng IQR Triming and Capping method got removed.
* Created dummie variable for categorical data.
* Perform Log Transformation futher on in Weekly sales, temperature, fuel price, cpi and unemployment.
* Also perform stadarization of the data.

![graph1](./Images/og_q.png)
![graph1](./Images/sales_vs_store.png)
![graph1](./Images/annual_sales.png)
![graph1](./Images/outlier_sales.png)

## Modeling

First 4 models where in great succes just in terms of r-squared value performing till 0.977, mse in cross validation where sloly reduce but not enough to provide a satifactory result. I went back to analyse the data for further analysis and created new variables for future models mainly base on categorization of stores and segmentation of weekly sales by quarter.

![graph1](./Images/modelq3result.png)
![graph1](./Images/modelq3.png)

## Summary

Last Model provided the best fit for linear regression with an R-squared value of 0.805, meaning that it represents 80.5% of the data, validating it with T-test provided a Mean Squared Error value: 0.0377 and Cross Validation result: 0.087.

## Recommendation

Using last model, demand will increase quarterly and will be significantly higher during the last quarter of the year, store type format for small, medium and large stores will prepared Walmart for future demand and stock supply.

![graph1](./Images/q_type.png)

Demand amount will depend on the store size, the model tell us that lager the store the higher the demand and prepared for holiday days as they are a factor that will increase demand.

## Repository Structure

```
├── README.md                    <- The top-level README for reviewers of this project
├── Capstone_Walmart.ipynb       <- Narrative documentation of recommendations in Jupyter notebook
├── walmart_presentation.pptx    <- PDF version of project presentation
├── data                         <- Both sourced externally and generated from code
└── images                       <- Both sourced externally and generated from code
```
