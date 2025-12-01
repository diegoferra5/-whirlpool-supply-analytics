# 📄 **Technical Summary of the Project: Whirlpool D2C Business Intelligence**

This project implements a complete data analysis and processing pipeline designed for Whirlpool’s Business Intelligence challenge, focused on the **Direct-to-Consumer (D2C)** and **E-Commerce** channel. The goal is to transform raw data delivered in Excel/CSV files into structured, cleaned, and analytics-ready information stored in a SQL database, which will later serve as the foundation for executive dashboards and actionable insights.

---

## **1. Data Ingestion**

All data files provided by Whirlpool (CSV/Excel) will be loaded using Python.  
These anonymized datasets include:

- Transaction-level sales records (customer, product, date, hour)
- Product catalog information
- Customer attributes and platform activity
- Country, category, and time-based details

The ingestion process includes:

- Reading files with `pandas`
- Validating table structure and column names
- Converting and standardizing data types (dates, numeric, categorical)
- Harmonizing schema across files

---

## **2. Data Exploration and Understanding**

A thorough exploratory analysis will be performed to understand:

- The granularity of each dataset
- Table relationships (natural keys, join conditions)
- Temporal behavior of sales and customer activity
- Emerging patterns within the D2C business (seasonality, categories, country behavior)

This phase includes technical checks such as:

- Record counts and summary statistics
- Null value distribution
- Outlier and anomaly detection
- Data consistency between tables
- Catalog mapping and semantic interpretation

---

## **3. Data Cleaning and Conditioning**

Based on business rules and exploration findings, the cleaning stage will include:

- Handling and correcting missing values
- Fixing inconsistent formats and data types
- Standardizing categories and labels
- Removing duplicate and invalid records
- Generating new analytical attributes:
  - Year, month, day, week
  - Customer country/region fields
  - Product category enrichments
  - Activity/reactivation flags
- Computing essential metrics:
  - Total sales
  - Active customers
  - New customers / reactivations
  - Category and country contribution
  - Time-based trends

---

## **4. SQL Data Loading**

After the data is cleaned, enriched, and validated, the final dataset will be loaded into a SQL database. This includes:

- Establishing a connection via `sqlalchemy`
- Creating destination tables with the proper schema
- Efficient bulk insertion of the processed data
- Post-load integrity checks (record counts, data types, missing values)

This SQL-ready table will serve as the foundation for:

- The Dimensional Model (fact and dimension tables)
- Executive dashboards and KPIs

---

## **5. Business Context**

Whirlpool’s D2C channel requires deeper understanding of:

- How customers behave over time (activity, frequency, reactivation patterns)
- Which categories and products drive performance
- Differences in sales behavior by country and season
- Trends and relationships that are not visible without advanced analytics

A clean, structured, and well-modeled dataset will enable dashboards that support:

- Better decision-making
- Identification of high-opportunity segments and categories
- Improved consumer experience
- Enhanced visibility into digital sales performance

---

If you want, I can also generate a **GitHub-ready README.md version**, or create a recommended folder structure for your entire pipeline (`/src`, `/data`, `/sql`, `/docs`, etc.).
