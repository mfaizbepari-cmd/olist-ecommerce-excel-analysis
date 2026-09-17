# Olist E-Commerce Analytics

## Project Objective

This project analyzes Brazilian e-commerce data using Excel to understand sales performance, customer behavior, delivery performance, payment methods, product categories, and customer reviews.

The project was built as an end-to-end Data Analyst workflow, starting from raw data and ending with an interactive Excel dashboard.

## Dataset

The project uses the Olist Brazilian E-Commerce Public Dataset.

The dataset contains multiple related tables covering:

- Customers
- Orders
- Order Items
- Payments
- Reviews
- Products
- Sellers
- Geolocation
- Product Category Translation

## Tools Used

- Microsoft Excel
- Power Query
- Power Pivot
- DAX
- PivotTables
- PivotCharts
- Excel formulas
- Slicers

## Data Preparation

The raw data was imported into Power Query and checked for:

- Missing values
- Duplicate records
- Data types
- Key integrity
- Foreign-key relationships
- Timeline anomalies
- Payment anomalies

Power Query was also used to:

- Standardize data types
- Merge product categories with the English translation table
- Remove exact duplicate geolocation records
- Create a ZIP-prefix geolocation lookup
- Enrich customer and seller geographic information
- Create delivery and data-quality flags
- Create order-level item, payment, and review summaries

## Data Model

A relational Data Model was created in Power Pivot.

Main relationships include:

- Customers → Orders
- Orders → Order Items
- Orders → Payments
- Orders → Reviews
- Products → Order Items
- Sellers → Order Items

The model was designed to maintain the correct grain of each table and avoid double counting.

## Exploratory Data Analysis

The analysis covered:

- Monthly sales trends
- Monthly order volume
- Product category performance
- State and city sales
- Delivery performance
- Delivery duration
- Payment methods
- Review score distribution
- Seller performance
- Repeat customer behavior
- Category average selling price

## KPI Measures

Key Data Model measures include:

- Total Orders
- Total Product Sales
- Average Order Value
- Unique Customers
- Total Items Sold
- Average Review Score
- Average Delivery Days
- On-Time Delivery Rate
- Late Delivery Rate
- Repeat Customer Rate

## Interactive Dashboard

The final dashboard provides an overview of:

- Sales
- Orders
- Customers
- Delivery performance
- Product categories
- Geographic performance
- Payment methods
- Customer reviews

A Year slicer was connected to the dashboard visuals and KPI measures to make the dashboard interactive.

## Business Insights

Key findings from the analysis are documented in:

`business_insights.md`

## Limitations

- The dataset covers a historical period from 2016 to 2018.
- September 2018 is a partial month.
- Some source columns contain missing values.
- Some delivery and review metrics depend on the availability of the underlying records.
- The analysis focuses on product sales and does not represent profitability because cost/profit data is not available.

## Project Structure

```text
olist-ecommerce-excel-analysis/

├── data/
│   └── raw/
│
├── excel/
│   └── Olist_Ecommerce_Analytics.xlsx
│
├── Documentation/
│   ├── data_quality_audit.md
│   ├── data_dictionary.md
│   ├── business_insights.md
│   └── project_overview.md
│
├── screenshots/
│   ├── power-query/
│   ├── data-model/
│   ├── eda/
│   └── dashboard/
│
└── README.md