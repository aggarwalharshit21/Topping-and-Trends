1. Project Title:   
   Pizza Sales Analysis Using MySQL

2. Project Description:   
   This project involves analyzing a pizza sales dataset using MySQL. The objective is to extract insights regarding sales trends, customer preferences, and business performance. It focuses on performing queries to analyze sales data and generate meaningful reports to help businesses improve decision-making.

3. Features:   
   - Sales trend analysis based on time, pizza type, and size.
   - Customer demographics analysis.
   - Revenue and sales performance analysis.
   - Query optimization for faster results.
   - Data visualization using SQL queries.

4. Technologies Used:
   - MySQL
   - SQL Queries
   - Database design principles
  
5. Database Structure:   
   The database contains the following key tables:
   - `Customers`: Stores customer information such as ID, name, and contact details.
   - `Orders`: Stores order information, including order ID, date, and customer ID.
   - `Pizzas`: Stores pizza details like type, size, and price.
   - `OrderDetails`: Connects orders and pizzas, capturing order quantity and specific pizza details.
     
6. Setup Instructions:
   a) Clone the repository:
   ```bash
   git clone https://github.com/username/pizza-sales-mysql.git
   ```
   b) Import the SQL schema:
   - Use the `pizza_sales_schema.sql` file to create and populate the database.
   - Run the script in your MySQL environment:
     ```sql
     source pizza_sales_schema.sql;
     ```

   c) Modify the connection parameters in your MySQL client if necessary (e.g., user, password).
   
7. Usage
   Example Queries:
   Total sales by pizza type:
   ```sql
   SELECT pizza_type, SUM(price) AS total_sales
   FROM Orders
   JOIN OrderDetails ON Orders.order_id = OrderDetails.order_id
   JOIN Pizzas ON OrderDetails.pizza_id = Pizzas.pizza_id
   GROUP BY pizza_type;
   ```

   - Revenue over time:
   ```sql
   SELECT order_date, SUM(price) AS daily_revenue
   FROM Orders
   JOIN OrderDetails ON Orders.order_id = OrderDetails.order_id
   GROUP BY order_date;
   ```
   
8. Contributing:
   Contributions are welcome! Please fork the repository and submit a pull request with a description of your changes.
   

9. Contact Information 
   Created by Harshit Aggarwal - [Email](mailto:ha2884730@gmail.com)
   
