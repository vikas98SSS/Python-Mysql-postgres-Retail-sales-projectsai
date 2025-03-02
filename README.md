# Vikas Dhakad
# Python-Mysql-postgres-Retail-sales-project


**Step-by-Step Description of the Python and SQL Project**

1. **Establishing Database Connection**
   - Import necessary libraries:
     - `pandas` for data manipulation.
     - `os` for file path operations.
     - `psycopg2` for PostgreSQL database connection.
   - Define the connection parameters and establish a connection to the PostgreSQL database named "ecommerce".

2. **Defining CSV Files and Corresponding Table Names**
   - Create a list of tuples containing CSV file names and their corresponding database table names:
     - `customers.csv` -> `customers`
     - `orders.csv` -> `orders`
     - `sellers.csv` -> `sellers`
     - `products.csv` -> `products`
     - `geolocation.csv` -> `geolocation`
     - `payments.csv` -> `payments`
     - `order_items.csv` -> `order_items`

3. **Reading and Processing CSV Files**
   - Define the folder path where the CSV files are stored.
   - Create a function `get_sql_type(dtype)` to determine the SQL data type based on the DataFrame column data type.
   - Loop through each CSV file and its corresponding table name:
     - Read the CSV file into a pandas DataFrame.
     - Replace NaN values with None to handle SQL NULL values.
     - Print the number of NaN values before replacement for debugging.
     - Clean column names by replacing spaces, dashes, and dots with underscores.

4. **Creating Database Tables**
   - Generate a SQL `CREATE TABLE` statement based on the DataFrame's columns and their corresponding SQL data types.
   - Execute the `CREATE TABLE` statement to create the table in the database if it does not already exist.

5. **Inserting Data into Database Tables**
   - For each row in the DataFrame, convert the row to a tuple and handle NaN/None values explicitly.
   - Construct an SQL `INSERT INTO` statement to insert the data into the corresponding table.
   - Execute the `INSERT` statement for each row.
   - Commit the transaction to save the changes to the database.

6. **Closing the Database Connection**
   - After processing all CSV files, close the database connection to free up resources.

7. **Executing SQL Queries for Data Analysis**
   - Various SQL queries are executed to analyze the data, including:
     - Listing unique cities where customers are located.
     - Counting the number of orders placed in 2017.
     - Finding total sales per product category.
     - Calculating the percentage of orders paid in installments.
     - Counting the number of customers from each state.
     - Analyzing orders per month in 2018.
     - Calculating average products per order grouped by customer city.
     - Analyzing revenue contribution by product category.
     - Identifying correlation between product price and purchase frequency.
     - Ranking sellers by total revenue generated.
     - Calculating moving averages of order values for customers.
     - Analyzing cumulative sales per month for each year.
     - Calculating year-over-year growth rates of total sales.
     - Evaluating customer retention rates.
     - Identifying top customers by spending in each year.

8. **Data Visualization**
   - Use libraries like `matplotlib` and `seaborn` to visualize the results of the analyses, such as bar charts for customer counts by state, orders per month, and top customers by sales.

This structured approach allows for efficient data processing and analysis, leveraging both Python and SQL capabilities.
Thanks for showing intrest in my project 
