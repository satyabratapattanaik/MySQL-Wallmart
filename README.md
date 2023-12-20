# MySQL-Walmart Sales Data Analysis

# About
This project explores Walmart Sales data to understand top-performing branches and products, sales trends of different products, and customer behaviour. The aim is to study how sales strategies can be improved and optimized.

# Purposes Of The Project
The major aim of this project is to gain insight into the sales data of Walmart to understand the different factors that affect sales of the different branches.

# About data
The dataset was obtained from the Kaggle Walmart Sales Forecasting Competition. This dataset contains sales transactions from three different branches of Walmart, respectively located in Mandalay, Yangon and Naypyitaw. The data contains 17 columns and 1000 rows:



|Column|Description|Data Type|
|:----:|:---------:|:-------:|
|invoice_id|Invoice of the sales made|VARCHAR(30)|
|branch|Branch at which sales were made|VARCHAR(5)|
|city|The location of the branch|VARCHAR(30)|
|customer_type|The type of the customer|VARCHAR(30)|
|gender|Gender of the customer making purchase|VARCHAR(10)|
|product_line|Product line of the product sold|VARCHAR(100)|
|unit_price|The price of each product|DECIMAL(10, 2)|
|quantity|The amount of the product sold|INT|
|VAT|The amount of tax on the purchase|FLOAT(6, 4)|
|total|The total cost of the purchase|DECIMAL(10, 2)|
|date|The date on which the purchase was made|DATE|
|time|The time at which the purchase was made|TIMESTAMP|
|payment_method|The total amount paid|DECIMAL(10, 2)|
|cogs|Cost Of Goods sold|DECIMAL(10, 2)|
|gross_margin_percentage|Gross margin percentage|FLOAT(11, 9)|
|gross_income|Gross Income|DECIMAL(10, 2)|
|rating|Rating|FLOAT(2, 1)|


# Approach Used

1. Data Wrangling: This is the first step where inspection of data is done to make sure NULL values and missing values are detected and data replacement methods are used to replace, 
   missing or NULL values.
   
   a. Build a database. <br>
   b. Create a table and insert the data. <br>
   c. Select columns with null values in them. There are no null values in our database as in creating the tables, we set NOT NULL for each 
   field, hence null values are filtered out. <br>
   
2. Feature Engineering: This will help us generate some new columns from existing ones.
   
   a. Add a new column named <b>time_of_date</b> to give an insight into sales in the Morning, Afternoon and Evening. This will help answer 
   the question of which part of the day most sales are made. <br>
   b. Add a new column named <b>day_name</b> that contains the extracted days of the week on which the given transaction took place (Mon, 
   Tue, Wed, Thur, Fri). This will help answer the question of which week of the day each branch is busiest. <br>
   c. Add a new column named <b>month_name</b> that contains the extracted months of the year on which the given transaction took place 
   (Jan, Feb, Mar). Help determine which month of the year has the most sales and profit. <br>



