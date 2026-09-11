# 🛒 Zepto E-commerce SQL Data Analysis Project

## 📌 Project Overview

This project focuses on analyzing a Zepto e-commerce inventory dataset using **SQL and PostgreSQL**. The purpose of the project is to understand how SQL can be applied to real-world data for exploration, cleaning, transformation, and business analysis.

The project follows a practical data analytics workflow, beginning with database and table creation, followed by data exploration, data cleaning, and analysis to identify useful business insights.

---

## 🎯 Project Objectives

The key objectives of this project include:

* Building and organizing an e-commerce inventory database using SQL
* Importing and working with a real-world inventory dataset
* Conducting Exploratory Data Analysis (EDA)
* Finding missing, duplicate, and inconsistent records
* Cleaning and preparing the data for analysis
* Studying product prices and discount patterns
* Analyzing stock availability and inventory levels
* Extracting meaningful business insights through SQL queries
* Strengthening practical SQL and data analytics skills

---

## 📊 Dataset Description

The dataset represents product-level inventory information from **Zepto's e-commerce platform**.

Each record represents a **SKU (Stock Keeping Unit)** and contains details related to the product, pricing, discounts, inventory, availability, and package size.

| Column                   | Description                                     |
| ------------------------ | ----------------------------------------------- |
| `sku_id`                 | Unique identification number for each SKU       |
| `name`                   | Name of the product                             |
| `category`               | Category to which the product belongs           |
| `mrp`                    | Maximum Retail Price of the product             |
| `discountPercent`        | Discount percentage offered on the product      |
| `discountedSellingPrice` | Final selling price after applying the discount |
| `availableQuantity`      | Quantity currently available in inventory       |
| `weightInGms`            | Weight of the product in grams                  |
| `outOfStock`             | Indicates whether the product is out of stock   |
| `quantity`               | Number of units included in the package         |

**Dataset Source:** Kaggle – Zepto Inventory Dataset

---

## 🛠️ Tools & Technologies Used

* **PostgreSQL**
* **pgAdmin**
* **SQL**
* **CSV Dataset**
* **GitHub**

---

## 🔄 Project Workflow

### 1. Database & Table Creation

A PostgreSQL table was created to store and manage the Zepto inventory data using suitable data types for each column.

```sql
CREATE TABLE zepto (
    sku_id SERIAL PRIMARY KEY,
    category VARCHAR(120),
    name VARCHAR(150) NOT NULL,
    mrp NUMERIC(8,2),
    discountPercent NUMERIC(5,2),
    availableQuantity INTEGER,
    discountedSellingPrice NUMERIC(8,2),
    weightInGms INTEGER,
    outOfStock BOOLEAN,
    quantity INTEGER
);
```

### 2. Data Import

The CSV dataset was imported into PostgreSQL through **pgAdmin**.

During the import process, an encoding issue was encountered and resolved by saving the dataset in **CSV UTF-8 format** before importing it into the database.

### 3. Data Exploration

Initial SQL queries were performed to understand the structure and characteristics of the dataset.

The exploration included:

* Checking the total number of records
* Identifying available product categories
* Comparing in-stock and out-of-stock products
* Finding duplicate product names
* Checking for missing values
* Understanding SKU and product distribution

### 4. Data Cleaning

Several data preparation steps were performed before the analysis, including:

* Identifying invalid pricing records
* Removing products with zero MRP or selling prices
* Converting price values from paise into rupees
* Checking the dataset for consistency and accuracy

### 5. Business Analysis

SQL queries were developed to answer practical business questions, such as:

* Which products provide the highest discounts?
* Which high-priced products are currently unavailable?
* Which categories provide the best average discounts?
* What is the estimated potential revenue across product categories?
* Which products offer better value based on their price per gram?
* How much total inventory weight is held within each category?
* Which expensive products have comparatively low discounts?

---

## 📈 SQL Skills & Concepts Practiced

This project provided hands-on practice with several SQL concepts, including:

* `SELECT`
* `WHERE`
* `GROUP BY`
* `ORDER BY`
* `HAVING`
* Aggregate functions
* `CASE` statements
* Subqueries
* Common Table Expressions (CTEs)
* Window functions
* Data cleaning techniques
* Data type conversion
* Ranking and product categorization

---

## 💡 Business Insights

The analysis highlights how SQL can be used to understand different aspects of an e-commerce business, including:

* Pricing and discount strategies
* Product availability and inventory levels
* High-value products
* Category-level performance
* Potential revenue opportunities
* Price-to-weight value comparison
* Stock-out trends

Such analysis can help businesses make better decisions related to **pricing, inventory planning, product promotions, and overall business strategy**.

---

## 📂 Project Structure

```text
Zepto-SQL-Data-Analysis/
│
├── zepto_v2.csv
├── zepto_SQL_data_analysis.sql
└── README.md
```

---

## 🎓 Learning Outcomes

Working on this project helped me improve my practical knowledge of **PostgreSQL and SQL for Data Analytics**.

Beyond learning individual SQL commands, I gained a better understanding of how SQL can be used as a problem-solving tool to work with real-world datasets and convert raw data into **meaningful business insights**.

This project also gave me hands-on exposure to the overall data analytics process, from **data ingestion and cleaning to analysis and business interpretation**.
