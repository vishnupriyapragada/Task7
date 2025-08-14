# Basic Sales Summary from a Tiny SQLite Database

## 📌 Project Overview
This project demonstrates how to:
- Create and work with an SQLite database in Python
- Run SQL queries for data summarization
- Import SQL results into Pandas
- Display a basic sales summary
- Visualize sales revenue using Matplotlib

The dataset contains technical products (laptops, monitors, accessories, etc.) with their quantity and price details.  
The project outputs both a tabular summary and a sales chart.

---

## 🛠 Tools & Libraries Used
- **Python 3**
- **SQLite3** (built-in with Python)
- **Pandas** (for data manipulation)
- **Matplotlib** (for visualization)

---

## 📂 Files
- `sales_data.db` → SQLite database file containing the `sales` table.
- `sales_summary.py` → Python script for creating the database, inserting data, querying, and plotting results.
- `sales_chart.png` → Generated bar chart for revenue by product.

---

## 📊 SQL Query Used
```sql
SELECT product,
       SUM(quantity) AS total_qty,
       SUM(quantity * price) AS revenue
FROM sales
GROUP BY product;
