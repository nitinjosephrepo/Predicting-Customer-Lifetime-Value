# Predicting 3 Month CLV from Ecommerce Customer Purchase Data

## Customer Life Time Value

In Marketing, the CLV is one of the key metrics to have and monitor. The CLV measures customer's total worth to the business over the course of their lifetime
relationship to a business. This metrif is especially important to keep track of for acquiring new customers. It's generally more expensive to acquire
new customers than to keep existing customers, so knowing thier lifetime value and the cost associated with the acquiring new customers is essential 
in order to build marketing strategies with a positve ROI. 


## Using Machine Learning to Predict CLV

Because, we do not typically know the lifetime span of customers, we often try to estimate CLV over the course of an certain period. It can be done by estimating
a customer's 12-month CLV, 24-month CLV, or can also be a 3-Month CLV. 

In this example our objective is to build a machine learning regression model to predict 3-month CLV from a Ecommerce Dataset. Being able to predict and 
understand the Customer Lifetime Value for individual customers help marketers

1. Justify their marketing budget
2. As well as target potential High-value Customers 

## Steps to Building a Regression Model to Predict CLV

1. Import Ecommerce Data
2. Data Cleanup
   - Handling negative quantity 
   - Dropping NaN Records
   - Handling incomplete data
   - Computing total sales value
3. Data Analysis
4. Predicting the 3 Month CLV
   - Data prepration
   - Linear Regression
   - Evaluating regression model performance
   
 ## Interpreting the Results 
  

| Feature       | coef          |
| ------------- |:-------------:| 
| sales_avg_M_2 | 0.250985      | 
| sales_avg_M_3 |-0.473740      |   
| sales_avg_M_4 |-0.261884      |     
| sales_avg_M_5 |-0.993126      |
|sales_count_M_2| 47.498205     |   
|sales_count_M_3|-21.651040     |   
|sales_count_M_4|-82.356524     |
|sales_count_M_5|-73.658176     | 
|sales_sum_M_2  | 0.159443      |
|sales_sum_M_3  | 0.400985      |
|sales_sum_M_4  | 0.266139      |
|sales_sum_M_5  | 1.255455      | 

As we can see from the coeffficient output, we can easily find which features have a negative correlation with the target( 3-month customer value) and which features have positive 
correlation with the target. 

**For example 2nd & 3rd & 4th most recent 3 months (Sales_avg_M_4, Sales_avg_M_5, Sales_avg_5) have a negative impact on the next 3 month customer value.
This means that the higher the purchase amount in M_3,M_4 and M_5 the lower the next 3 month purchase is going to be. On the other hands the most recent 
3-month (Sales_avg_M_2) is positively correlated with the next 3 month customer value.** 

*In other words, the more a customer made purchases in the last 3 months, the higher value he or she will bring in next 3 months.*

Using the 3 month customer value prediction output, we can than custom-tailor our marketing strategies in different ways. Since we now know the expected revenue
or purchase amount from individual customers for the next 3 months, we can set a better informed budget for the marketing campaigns. 

On the other hands, we can also use the 3 months customer value prediction output values to specifically target these high-value customers for the next 
3 months. 
