# Electronic-Store-s-Sales-Analysis-Python

## Link to Dataset used by this project:

https://github.com/KeithGalli/Pandas-Data-Science-Tasks/tree/master/SalesAnalysis/Sales_Data

## Dataset: A whole year sales data of an US electronic store breakdown by month

## Cleaning Data (Pandas):

Merge monthly sales data (12 csv files) into one csv file
Find Nan data and drop them
Extract additional information from current columns as new columns ('Month','Sales','City','Hour')
Change data type using pd.to_numeric/pd.to_datetime/.astype('int')

## 5 Business Questions:

1. What was the best month for sales? How much was earned that month?

Dataset groupby 'Month' column, plot bar chart with x-axis as month, y-axis as sales

Conclusion: 

December is the best month of sales because of holiday seasons in US, the total earning rocket to 4.6 million dollars!

2. What city has the highest sales?

Dataset groupby 'City (State)' column to aviod duplicate city names, plot bar chart with x-axis as city name, y-axis as sales

Conclusions: 

San Francisco ranked the 1st place in sales

The Silicon Valley located in San Francisco, huge demands for electronic instruments

People with higher income level try to experience cutting edge technology
             
3. What time should we display advertisments to maximize likelihood of customer's buying product?

Extract Hour from Order Date column, and count orders after groupby hour, plot line chart with x-axis as hour, y-axis as number of orders

Conclusions: 

Recommendation time is around 11-12 AM or 7PM

4. What products are most often sold together?

stack overflow reference: https://stackoverflow.com/questions/52195887/counting-unique-pairs-of-numbers-into-a-python-dictionary

There are duplicated orders with same 'Order ID' but different 'Product'

Grouped 'Product' together with the same 'Order ID' and drop duplicates

Import two new libraries to count unique pairs of products:

from itertools import combinations

from collections import Counter

Conclusions: 

Bundling sales of iphone or Google Phone and lighting charging cable is the most attractive promotion method

5. What product sold the most ? Why do you think it sold the most?

Dataset groupby product and plot bar chart with x-axis as product, y-axis as quantity ordered

Plot twinx chart to find relationships between price and quantity ordered

Conclusion: 

AAA Batteries & AAatteries sold the most because of its utility function and cheap price 

The negative correlations between quantity ordered and prices, the prices turn up and orders turn down as normal trend

For some particular products like Macbook Pro Laptop, its quantity higher than some of other products while its price is is the highest,

this is may because people are now expect to experience new technology and value the perfomance of products when they consume

