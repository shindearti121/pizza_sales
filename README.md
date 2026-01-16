# 🍕 Pizza Sales Analysis (SQL Project)

## 📌 Project Overview
This project focuses on analyzing pizza sales data using **SQL** to gain business insights such as total revenue, best-selling pizzas, customer ordering patterns, and category-wise performance.

The dataset contains detailed information about orders, pizzas, pizza types, and order details. SQL queries are used to answer real-world business questions.

---

## 📂 Dataset Description
The project uses the following CSV files:

- **orders.csv** – Contains order ID, date, and time  
- **order_details.csv** – Contains order ID, pizza ID, and quantity  
- **pizzas.csv** – Contains pizza ID, pizza type, size, and price  
- **pizza_types.csv** – Contains pizza name, category, and ingredients  

---

## 🛠️ Tools & Technologies Used
- **SQL (MySQL / PostgreSQL compatible)**
- **CSV Data**
- **Git & GitHub**

---

## 📊 Key Analysis Performed
- Total number of orders
- Total revenue generated
- Most and least sold pizzas
- Revenue by pizza category
- Order distribution by time and date
- Average order value
- Top 5 pizzas by sales quantity
- Size-wise pizza demand

---

## 🧠 Sample SQL Queries
```sql
-- Total Revenue
SELECT 
    ROUND(SUM(od.quantity * p.price), 2) AS total_revenue
FROM order_details od
JOIN pizzas p ON od.pizza_id = p.pizza_id;
