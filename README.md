# Credit Card Dashboard Project

## Table of Contents

- [Overview](#overview)
- [Objectives](#objectives)
- [Project Level](#project-level)
- [Data Sources](#data-sources)
- [Methodology](#methodology)
- [Dashboard Components](#dashboard-components)
  - [Credit Card Transaction Report](#credit-card-transaction-report)
  - [Credit Card Customer Report](#credit-card-customer-report)
- [Tools and Technologies](#tools-and-technologies)
- [Conclusion](#conclusion)

## Overview
The Credit Card Dashboard Project is a dynamic data visualization solution developed using Power BI. It integrates multiple data sources and uses SQL scripts to update a MySQL database, ensuring that the dashboard always reflects the latest information. This project provides a comprehensive view of credit card transactions and customer insights, empowering stakeholders to make data-driven decisions.

## Objectives

- **Analyze Credit Card Transactions:**  
  Visualize key financial metrics such as revenue, total transaction amounts, and interest earned across various credit card categories.

- **Segment Customer Data:**  
  Analyze customer demographics (e.g., job, income, age) to understand spending behaviors and revenue contributions.

- **Dynamic Data Updates:**  
  Use SQL to update the MySQL database with new records from supplemental CSV files, keeping the dashboard data current.

## Project Level
**Intermediate**  
This project is designed for users with intermediate knowledge of data integration, SQL, and Power BI dashboard development. It demonstrates effective data merging, database updating techniques, and interactive visualization strategies.

## Data Sources

The project utilizes four CSV files:

- **credit_card.csv:**  
  Primary dataset containing historical credit card transaction data.

- **cc_add.csv:**  
  Supplemental data providing additional credit card transaction records.

- **Customers.csv:**  
  Primary dataset with customer demographics and revenue-related information.

- **cust_add.csv:**  
  Supplemental data providing additional customer records.

## Methodology

1. **Data Acquisition:**  
   - Import the primary CSV files (`credit_card.csv` and `Customers.csv`) into the MySQL database to create the base datasets.
   - Load additional records from `cc_add.csv` and `cust_add.csv` into temporary tables for later merging.

2. **Database Integration:**  
   - **Initial Load:**  
     Establish the baseline datasets using the primary CSV files.
   - **Data Updates:**  
     Use SQL scripts to merge new records into the existing tables. For example:
     ```sql
     -- Update credit card transactions from cc_add.csv
     INSERT INTO credit_card_table (card_id, revenue, total_trans_amt, interest_earned)
     SELECT card_id, revenue, total_trans_amt, interest_earned
     FROM temporary_cc_add;
     ```
     ```sql
     -- Update customer records from cust_add.csv
     INSERT INTO customers_table (customer_id, job, revenue, income, interest_earned)
     SELECT customer_id, job, revenue, income, interest_earned
     FROM temporary_cust_add;
     ```

3. **Dashboard Development:**  
   - **Design & Build:**  
     Create interactive reports and visualizations in Power BI based on the updated MySQL database.
   - **Data Refresh:**  
     Regularly refresh the dashboard to reflect the latest updates from the database.

## Dashboard Components

### Credit Card Transaction Report

- **Card Category Analysis:**  
  Detailed visualizations for different card categories (Platinum, Gold, Silver, Blue) displaying revenue, transaction volumes, and interest earned.

- **Trend Analysis:**  
  Quarterly revenue and transaction trends along with regional performance insights.

### Credit Card Customer Report

- **Customer Segmentation:**  
  Breakdown of customer data by job type, income, and other demographics.

- **Interactive Visualizations:**  
  Time series charts, age-based revenue analysis, and other metrics to support data-driven decision-making.

## Tools and Technologies

- **Power BI Desktop:**  
  For designing and building interactive dashboards.
- **MySQL Database:**  
  Acts as the central data repository for storing and updating CSV data.
- **SQL:**  
  Used to update and merge data into the MySQL database.
- **CSV Files:**  
  Four primary files (`credit_card.csv`, `cc_add.csv`, `Customers.csv`, `cust_add.csv`) form the core data sources.

## Conclusion

The Credit Card Dashboard Project integrates multiple data sources with dynamic SQL-driven updates to provide an up-to-date, interactive Power BI dashboard. This project enhances the understanding of credit card transactions and customer insights while demonstrating effective data integration and visualization techniques suitable for intermediate users.
