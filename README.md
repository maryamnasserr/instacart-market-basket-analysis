# Instacart Market Basket Analysis using Apache Spark

## Overview
This project analyzes the Instacart Market Basket dataset using Apache Spark. It focuses on understanding customer purchasing behavior, product demand patterns, and department-level performance through large-scale data processing.

The dataset consists of multiple relational tables, which were integrated into a unified dataset to enable end-to-end analysis using both Spark DataFrame API and Spark SQL.

---

## Dataset
The dataset is sourced from Kaggle and contains real-world Instacart transactional data:

- orders: customer order metadata (day, hour, frequency)
- order_products__prior: products in previous orders
- order_products__train: products in training orders
- products: product details
- aisles: product aisle categories
- departments: product department categories

Source: Instacart Market Basket Analysis (Kaggle)

---

## Project Objectives
- Initialize and configure a Spark session
- Load and integrate multiple relational datasets
- Clean and validate data after each preprocessing step
- Create a unified analytical dataset
- Engineer behavioral features to understand customer patterns
- Perform business analysis using Spark DataFrame API and Spark SQL
- Extract actionable insights for decision-making

---

## Technologies Used
- Apache Spark (PySpark)
- Spark SQL
- Python
- Pandas
- KaggleHub

---

## Project Workflow

### 1. Spark Session Initialization
- Created and configured SparkSession for distributed processing

### 2. Data Loading
- Loaded Instacart datasets using KaggleHub
- Imported multiple CSV files into Spark DataFrames

### 3. Data Exploration & Validation
- Checked schema consistency across datasets
- Identified missing values
- Validated data integrity after each transformation

### 4. Data Preprocessing
- Handled missing values (e.g., days_since_prior_order)
- Removed duplicate records
- Converted data types using safe casting (`try_cast`)

### 5. Data Integration
- Merged order_products__prior and order_products__train
- Joined orders, products, aisles, and departments
- Created a unified dataset for analysis

### 6. Feature Engineering
- Total items per order
- Reorder ratio per order
- Customer order frequency

---

## Analysis Performed

All analyses were implemented using both Spark DataFrame API and Spark SQL.

### a) Top Departments by Orders
Identified departments with the highest number of ordered products.

### b) Reorder Rate by Department
Measured customer loyalty through reorder frequency per department.

### c) Peak Shopping Hours
Analyzed order distribution across hours of the day to identify demand peaks.

### d) Average Basket Size
Calculated average number of items per order to understand purchasing behavior.

### e) Top Reordered Products
Identified products with highest reorder counts, mainly essential grocery items.

### f) Department Contribution
Calculated percentage contribution of each department to total orders.

---

## Machine Learning
No machine learning models were applied. The focus was on big data processing, transformation, and analytical insights using Spark.

---

## User Segmentation (Bonus Task)
Users were segmented based on order frequency into:
- Low Activity Users
- Medium Activity Users
- High Activity Users

This helps identify customer engagement levels.

---

## Key Findings
- Produce, dairy & eggs, and snacks dominate order volume
- Dairy & eggs and beverages show the highest reorder rates
- Peak shopping occurs between 10 AM and 4 PM
- Average basket size is ~15–16 items per order
- A small number of essential products drive most reorder behavior
- A few departments dominate total contribution

---

## Repository Contents
```text
├── DataFrame.ipynb
├── SQL.ipynb
└── README.md
