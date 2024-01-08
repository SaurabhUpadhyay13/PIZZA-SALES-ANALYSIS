# PIZZA-SALES-ANALYSIS

Overview<br>

Welcome to the Pizza Sales Analysis project repository! This project explores the world of pizza sales through a comprehensive data analysis, revealing insights that go beyond the crust. Leveraging the power of <br>
MySQL and Power BI, this repository showcases a deep dive into key performance indicators (KPIs), monthly trends, and categorical analyses to provide a holistic view of pizza sales data.
<br>
<br>

Features

<br><br>
Key Performance Indicators (KPIs)<br><br>
Total Revenue:<br>
SQL Query: SELECT ROUND(SUM(total_price), 2) AS Total_Revenue FROM pizza_sales;<br>
Unveiling the financial success by summing up total sales.<br><br>
Average Order Value:<br>
SQL Query: SELECT ROUND(SUM(total_price) / COUNT(DISTINCT order_id), 2) AS Avg_order_value FROM pizza_sales;<br>
Analyzing the average value per order to understand customer spending patterns.<br><br>
Total Pizzas Sold:<br>
SQL Query: SELECT SUM(quantity) AS Total_pizza_sold FROM pizza_sales;<br>
Revealing the total quantity of pizzas sold, a key metric for demand.<br><br>
Total Orders:<br>
SQL Query: SELECT COUNT(DISTINCT order_id) AS Total_orders FROM pizza_sales;<br>
Counting distinct orders to understand the overall order volume.<br><br>
Average Pizzas Per Order:<br>
SQL Query: SELECT ROUND(SUM(quantity) / COUNT(DISTINCT order_id), 2) AS Avg_pizzas_per_order FROM pizza_sales;<br>
Calculating the average number of pizzas per order, a crucial insight for inventory management.<br><br>
Monthly Trend for Total Orders<br>
SQL Query: SELECT MONTHNAME(STR_TO_DATE(order_date, '%Y-%m-%d')) AS order_day, COUNT(DISTINCT order_id) AS total_order FROM pizza_sales GROUP BY order_day;<br>
Unveiling the monthly trends in total orders, helping identify peak sales periods.<br><br>
Percentage Sales by Pizza Category<br>
SQL Query: SELECT pizza_category, ROUND(SUM(total_price), 2) AS total_revenue, SUM(total_price) * 100 / (SELECT SUM(total_price) FROM pizza_sales) AS PCT FROM pizza_sales GROUP BY pizza_category;<br>
Analyzing sales distribution across different pizza categories, providing insights into customer preferences.<br><br>
Percentage Sales by Pizza Size<br>
SQL Query: SELECT pizza_size, ROUND(SUM(total_price), 2) AS total_revenue, ROUND(SUM(total_price) * 100 / (SELECT SUM(total_price) FROM pizza_sales), 2) AS PCT FROM pizza_sales GROUP BY pizza_size;<br>
Breaking down sales by pizza size, allowing for strategic marketing decisions.<br><br>
Software Used<br>
MySQL: Utilized for robust data querying and manipulation.<br>
Power BI: Transformed raw data into visually compelling and interactive dashboards.<br>
Dashboard Development: Crafted dynamic visualizations to highlight key KPIs and trends.<br><br>
How to Use<br>
Clone the repository to your local machine.(git clone "Path of this file") **type this to your terminal**<br>
Import the provided database (pizza_sales.csv) into your MySQL server.<br>
Open the Power BI file (pizza_sales_analysis.pbix) to explore the interactive dashboard.<br><br>
Feel free to explore, analyze, and customize the project as needed. If you have any questions or suggestions, please don't hesitate to reach out.<br><br>

Happy analyzing! 🍕📊


