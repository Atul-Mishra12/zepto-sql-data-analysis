# 🛒 Zepto Inventory Analysis using PostgreSQL

A beginner-friendly SQL project where I explored, cleaned and analysed Zepto's product inventory data to answer common business questions about pricing, discounts and stock.

## 📌 About the Project
After learning PostgreSQL, I built this project to practise the full SQL workflow: creating a table, importing data, exploring it, cleaning it, and writing queries to find insights.

## 📂 Dataset
- **Source:** [Zepto Inventory Dataset on Kaggle](https://www.kaggle.com/datasets/palvinder2006/zepto-inventory-dataset/data?select=zepto_v2.csv)
- **Size:** 3,732 rows (one row per product listing) across 14 categories
- **Columns:** category, name, mrp, discountPercent, availableQuantity, discountedSellingPrice, weightInGms, outOfStock, quantity
- Prices in the file are stored in **paise**, so I converted them to **rupees**.

## 🛠️ Tools Used
- PostgreSQL
- pgAdmin

## 🔄 What I Did

**1. Created the table and imported the data**
- Created the `zepto` table with suitable data types and a primary key
- Imported the CSV file into PostgreSQL

**2. Explored the data**
- Counted the total rows and viewed sample records
- Checked for NULL values in every column
- Listed the different product categories
- Compared in-stock and out-of-stock products
- Found product names that appear more than once

**3. Cleaned the data**
- Found products with a price of 0 and deleted them
- Converted `mrp` and `discountedSellingPrice` from paise to rupees

**4. Answered business questions with SQL**

| # | Question |
|---|---|
| 1 | Which 10 products have the highest discount? |
| 2 | Which high-MRP products (above ₹300) are out of stock? |
| 3 | What is the estimated revenue for each category? |
| 4 | Which products cost more than ₹500 but have less than 10% discount? |
| 5 | Which 5 categories have the highest average discount? |
| 6 | What is the price per gram of each product (for 100 g and above)? |
| 7 | How can products be grouped into Low, Medium and Bulk by weight? |
| 8 | What is the total inventory weight for each category? |
| 9 |Q9. Analyze Overstock vs Stockouts per Category |

## 🔍 Things I Noticed
- The dataset has 3,732 rows, and one row had a price of 0, which I removed.
- About 12% of the listings (453 rows) are out of stock.
- **Fruits & Vegetables** has the highest average discount (about 15%), followed by **Meats, Fish & Eggs** (about 11%).
- The same product often appears in more than one category, so category-level totals (like revenue and weight) can be inflated by repeated listings.

## 🧠 SQL Concepts Practised
`CREATE TABLE` · `SELECT` · `WHERE` · `GROUP BY` · `HAVING` · `ORDER BY` · `LIMIT` · `DISTINCT` · `CASE WHEN` · `SUM` · `AVG` · `ROUND` · `UPDATE` · `DELETE`

## 📁 Files in this Repository
- `zepto_sql_project.sql`: all the SQL code (table creation, exploration, cleaning, analysis)
- `zepto_v2.csv`: the dataset
- `README.md`: project description

## 🚀 How to Run
1. Create a new database in PostgreSQL.
2. Open the Query Tool in pgAdmin and run the `CREATE TABLE` statement from the SQL file.
3. Import `zepto_v2.csv` into the table (save it as CSV UTF-8 first if you get an encoding error).
4. Run the rest of the queries one section at a time.

## 🙏 Credits
- Project inspired by Amlan Mohanty's YouTube tutorial.
- Dataset from Kaggle.

## 📬 Connect
**Atul Mishra** · [LinkedIn](www.linkedin.com/in/contactatul)
