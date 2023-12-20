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
|time|The time at which the purchase was made|TIME|
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
   
   a. Add a new column named [ time_of_date ] to give an insight into sales in the Morning, Afternoon and Evening. This will help answer 
   the question of which part of the day most sales are made. <br>
   b. Add a new column named [ day_name ] that contains the extracted days of the week on which the given transaction took place (Mon, 
   Tue, Wed, Thur, Fri). This will help answer the question of which week of the day each branch is busiest. <br>
   c. Add a new column named [ month_name ] that contains the extracted months of the year on which the given transaction took place 
   (Jan, Feb, Mar). Help determine which month of the year has the most sales and profit. <br>


# Generic Question

1. How many unique cities does the data have?
2. In which city is each branch?
   
# Product

1. How many unique product lines does the data have?
2. What is the most common payment method?
3. What is the most selling product line?
4. What is the total revenue by month?
5. What month had the largest COGS?
6. What product line had the largest revenue?
7. What is the city with the largest revenue?
8. What product line had the largest VAT?
9. Which branch sold more products than average product sold?
10. What is the most common product line by gender?
11. What is the average rating of each product line?

    
# Sales

1. Number of sales made in each time of the day per weekday
2. Which of the customer types brings the most revenue?
3. Which city has the largest tax percent/ VAT (Value Added Tax)?
4. Which customer type pays the most in VAT?

   
# Customer

1. How many unique customer types does the data have?
2. How many unique payment methods does the data have?
3. What is the most common customer type?
4. Which customer type buys the most?
5. What is the gender of most of the customers?
6. What is the gender distribution per branch?
7. Which time of the day do customers give most ratings?
8. Which time of the day do customers give most ratings per branch?
9. Which day fo the week has the best avg ratings?
10. Which day of the week has the best average ratings per branch?

    
# Revenue And Profit Calculations

1. COGS = unit_price * quantity

   Example with the first row in our DB:<br>
   Data given:<br>
   a. unit_price = 45.79 <br>
   b. quantity = 7 <br>
   c. COGS = 45.79 * 7 = 320.53 <br>

2. VAT = 5% * COGS = 5% 320.53 = 16.0265 

   is added to the and this is what is billed to the customer.

3. total(gross_sales) = VAT + COGS = 16.0265 + 320.53 = 336.5565 

4. gross_profit(gross_income) = total(gross_sales) - COGS = 336.5565 - 320.53 = 16.0265

   Gross Margin is gross profit expressed in percentage of the total(gross_profit / revenue)

5. gross_margin = gross_income / total_revenue = 16.0265 / 336.5565  
                                               = 0.047619 
                                               \\ approx 4.7619%



