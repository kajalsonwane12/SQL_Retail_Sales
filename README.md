-- SQL Retail Sales Analysis

-- Create Database
CREATE DATABASE sql_project_1;
USE sql_project_1;

-- Create Table
CREATE Table Retail_Sales ( 
transaction_id INT NOT NULL,
sale_date DATE NOT NULL,
sale_time TIME NOT NULL,
customer_id INT NOT NULL,
gender VARCHAR(25) NOT NULL,
age INT NOT NULL,
category VARCHAR(25) NOT NULL,
quantity INT NOT NULL,
price_per_unit FLOAT NOT NULL,
cogs FLOAT NOT NULL,
total_sale FLOAT NOT NULL,
PRIMARY KEY (transaction_id,customer_id)
);

DESC Retail_Sales;

SELECT * FROM Retail_Sales;

INSERT INTO Retail_Sales 
(transaction_id, sale_date, sale_time, customer_id, gender, age, category, quantity, price_per_unit, cogs, total_sale)
VALUES
(180, '2022-11-05', '10:47:00', 117, 'Male', 41, 'Clothing', 3, 300, 129, 900),
(522, '2022-07-09', '11:00:00', 52, 'Male', 46, 'Beauty', 3, 500, 145, 1500),
(559, '2022-12-12', '10:48:00', 5, 'Female', 40, 'Clothing', 4, 300, 84, 1200),
(1180, '2022-01-06', '08:53:00', 85, 'Male', 41, 'Clothing', 3, 300, 129, 900),
(1522, '2022-11-14', '08:35:00', 48, 'Male', 46, 'Beauty', 3, 500, 235, 1500),
(1559, '2022-08-20', '07:40:00', 49, 'Female', 40, 'Clothing', 4, 300, 144, 1200),
(163, '2022-10-31', '09:38:00', 144, 'Female', 64, 'Clothing', 3, 50, 23, 150),
(303, '2022-04-22', '11:09:00', 54, 'Male', 19, 'Electronics', 3, 30, 14.7, 90),
(421, '2022-04-08', '08:43:00', 66, 'Female', 37, 'Clothing', 3, 500, 235, 1500),
(979, '2022-05-18', '10:18:00', 6, 'Female', 19, 'Beauty', 1, 25, 10.5, 25),
(1163, '2022-05-04', '10:52:00', 120, 'Female', 64, 'Clothing', 3, 50, 27, 150),
(1303, '2022-03-19', '08:59:00', 58, 'Male', 19, 'Electronics', 3, 30, 15, 90),
(1421, '2022-01-17', '07:07:00', 59, 'Female', 37, 'Clothing', 3, 500, 185, 1500),
(1979, '2022-08-17', '11:34:00', 102, 'Female', 19, 'Beauty', 1, 25, 7.75, 25),
(610, '2022-12-18', '06:56:00', 137, 'Female', 26, 'Beauty', 2, 300, 93, 600),
(1610, '2022-11-23', '10:18:00', 1, 'Female', 26, 'Beauty', 2, 300, 102, 600),
(32, '2022-07-16', '09:11:00', 150, 'Male', 30, 'Beauty', 3, 30, 8.4, 90),
(231, '2022-07-09', '07:02:00', 50, 'Female', 23, 'Clothing', 3, 50, 26.5, 150),
(683, '2022-03-06', '10:22:00', 82, 'Male', 38, 'Beauty', 2, 500, 175, 1000),
(1032, '2022-04-01', '08:15:00', 1, 'Male', 30, 'Beauty', 3, 30, 10.5, 90),
(1231, '2022-01-29', '07:05:00', 12, 'Female', 23, 'Clothing', 3, 50, 23, 150),
(1683, '2022-05-04', '07:19:00', 98, 'Male', 38, 'Beauty', 2, 500, 220, 1000),
(367, '2022-12-30', '07:03:00', 123, 'Female', 57, 'Electronics', 1, 50, 18, 50),
(391, '2022-03-25', '07:37:00', 68, 'Male', 19, 'Beauty', 2, 25, 6.25, 50),
(432, '2022-03-10', '11:31:00', 17, 'Female', 34, 'Electronics', 2, 500, 190, 1000),
(1367, '2022-04-15', '11:38:00', 16, 'Female', 54, 'Electronics', 1, 50, 15.5, 50),
(1391, '2022-03-01', '11:29:00', 130, 'Male', 34, 'Beauty', 2, 25, 9.25, 50),
(1432, '2022-12-25', '06:24:00', 67, 'Female', 23, 'Electronics', 2, 500, 245, 1000),
(150, '2022-04-13', '08:25:00', 89, 'Female', 23, 'Electronics', 4, 30, 16.2, 120),
(845, '2022-10-27', '10:12:00', 25, 'Male', 78, 'Clothing', 1, 500, 145, 500),
(1150, '2022-08-22', '10:04:00', 77, 'Female', 12, 'Electronics', 4, 30, 10.2, 120),
(1845, '2022-05-24', '07:06:00', 94, 'Male', 32, 'Clothing', 1, 500, 185, 500),
(797, '2022-09-16', '06:38:00', 116, 'Male', 89, 'Clothing', 3, 25, 10.75, 75),
(921, '2022-09-28', '09:34:00', 101, 'Male', 87, 'Electronics', 3, 25, 8, 75),
(1797, '2022-04-16', '11:47:00', 147, 'Male', 40, 'Clothing', 3, 25, 12.25, 75),
(1921, '2022-02-08', '07:01:00', 77, 'Male', 51, 'Electronics', 3, 25, 7.5, 75),
(291, '2022-11-22', '08:29:00', 15, 'Male', 60, 'Clothing', 2, 300, 126, 600),
(907, '2022-09-02', '06:16:00', 145, 'Female', 45, 'Electronics', 1, 25, 8.5, 25),
(1291, '2022-04-04', '11:19:00', 72, 'Male', 60, 'Clothing', 2, 300, 153, 600),
(1907, '2022-11-17', '11:21:00', 115, 'Female', 45, 'Electronics', 1, 25, 9, 25),
(860, '2022-04-11', '08:58:00', 85, 'Male', 63, 'Clothing', 4, 50, 16, 200),
(1860, '2022-03-12', '11:21:00', 57, 'Male', 63, 'Clothing', 4, 50, 18, 200),
(184, '2022-02-13', '06:44:00', 128, 'Male', 31, 'Electronics', 4, 50, 17, 200);

SELECT * FROM Retail_Sales;

-- Count all rows from the table
SELECT COUNT(*) FROM Retail_Sales;

-- Show only 10 records from the table
SELECT * FROM Retail_Sales LIMIT 10;

-- Data Cleaning

SELECT * FROM Retail_Sales
WHERE transaction_id IS NULL
OR sale_date IS NULL
OR sale_time IS NULL
OR gender IS NULL
OR category IS NULL
OR quantity IS NULL
OR cogs IS NULL
OR total_sale IS NULL;

DELETE FROM Retail_sales WHERE transaction_id IS NULL
OR sale_date IS NULL
OR sale_time IS NULL
OR gender IS NULL
OR category IS NULL
OR quantity IS NULL
OR cogs IS NULL
OR total_sale IS NULL;

-- Data Exploration

-- How many sales we have ?
SELECT COUNT(*) as total_sale FROM Retail_Sales;

-- How many unique Customers we have ?
SELECT COUNT(DISTINCT customer_id) FROM Retail_Sales;

-- Data Analysis & Business Key Problems & Answers

-- My Analysis & Findings
-- Q.1 Write a SQL query to retrieve all columns for sales made on '2022-11-05
SELECT * FROM Retail_Sales
WHERE sale_date = '2022-11-05';

-- Q.2 Write a SQL query to retrieve all transactions where the category is 'Clothing' and the quantity sold is more than 10 in the month of Nov-2022
SELECT * FROM Retail_Sales
WHERE category = 'Clothing'
AND quantity > 10
AND YEAR(sale_date) = 2022
AND MONTH(sale_date) = 11;

-- Q.3 Write a SQL query to calculate the total sales (total_sale) for each category.
SELECT category, SUM(total_sale) AS total_sales FROM Retail_Sales
GROUP BY category;

-- Q.4 Write a SQL query to find the average age of customers who purchased items from the 'Beauty' category.
SELECT avg(age) FROM Retail_Sales 
WHERE category = 'Beauty';

-- Q.5 Write a SQL query to find all transactions where the total_sale is greater than 1000.
SELECT transaction_id FROM Retail_Sales
WHERE total_sale > 1000;

-- Q.6 Write a SQL query to find the total number of transactions (transaction_id) made by each gender in each category.
SELECT gender,category,
COUNT(*) as total_transaction FROM Retail_Sales
GROUP BY gender,category
ORDER BY 1;

-- Q.7 Write a SQL query to calculate the average sale for each month. Find out best selling month in each year
SELECT 
    YEAR(sale_date) AS sale_year,
    MONTH(sale_date) AS sale_month,
    AVG(total_sale) AS avg_sale,
    RANK() OVER (PARTITION BY YEAR(sale_date) ORDER BY AVG(total_sale) DESC) AS rank_in_year
FROM Retail_Sales
GROUP BY YEAR(sale_date), MONTH(sale_date)
ORDER BY sale_year, rank_in_year;

-- Q.8 Write a SQL query to find the top 5 customers based on the highest total sales 
SELECT customer_id, SUM(total_sale) as Highest_Sales FROM Retail_Sales 
GROUP BY 1
ORDER BY 2 DESC 
LIMIT 5;

-- Q.9 Write a SQL query to find the number of unique customers who purchased items from each category.
SELECT category, COUNT(DISTINCT customer_id) as cnt_unique_cs FROM Retail_Sales
GROUP BY category; 

-- Q.10 Write a SQL query to create each shift and number of orders (Example Morning <=12, Afternoon Between 12 & 17, Evening >17)
WITH hourly_sale
AS
(
SELECT *,
    CASE
        WHEN EXTRACT(HOUR FROM sale_time) < 12 THEN 'Morning'
        WHEN EXTRACT(HOUR FROM sale_time) BETWEEN 12 AND 17 THEN 'Afternoon'
        ELSE 'Evening'
    END as shift
FROM retail_sales
)
SELECT 
    shift,
    COUNT(*) as total_orders    
FROM hourly_sale
GROUP BY shift
