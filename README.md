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
The Credit Card Dashboard Project is a dynamic data visualization solution developed using Power BI. It integrates multiple data sources and employs a direct import method to update a MySQL database, ensuring that the dashboard always reflects the latest information. This project provides a comprehensive view of credit card transactions and customer insights, empowering stakeholders to make data-driven decisions.

## Objectives

- **Analyze Credit Card Transactions:**  
  Visualize key financial metrics such as revenue, total transaction amounts, and interest earned across various credit card categories.

- **Segment Customer Data:**  
  Analyze customer demographics (e.g., job, income, age) to understand spending behaviors and revenue contributions.

- **Dynamic Data Updates:**  
  Update the MySQL database with new records from supplemental CSV files using MySQL's direct import features, keeping the dashboard data current.

## Project Level
**Intermediate**  
This project is designed for users with intermediate knowledge of data integration, SQL, and Power BI dashboard development. It demonstrates effective data merging, direct data importing into MySQL, and interactive visualization strategies.

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
   - Import the primary CSV files (`credit_card.csv` and `Customers.csv`) into the MySQL database to establish the base datasets.
   - Prepare the supplemental CSV files (`cc_add.csv` and `cust_add.csv`) for updating the existing tables.

2. **Database Integration:**  
   - **Initial Load:**  
     Establish the baseline datasets using the primary CSV files.
   - **Data Updates via Direct Import:**  
     Use MySQL's direct import method (such as the `LOAD DATA INFILE` command or MySQL Workbench's import feature) to load new records from the supplemental CSV files directly into the existing tables. This approach allows for quick updates without manually writing SQL INSERT scripts.

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
- **Direct Import Methods:**  
  Utilized to update the MySQL tables with new data from CSV files (e.g., using `LOAD DATA INFILE`).
- **CSV Files:**  
  Four primary files (`credit_card.csv`, `cc_add.csv`, `Customers.csv`, `cust_add.csv`) form the core data sources.

## Conclusion

The Credit Card Dashboard Project integrates multiple data sources with dynamic, direct import updates to provide an up-to-date, interactive Power BI dashboard. This project enhances the understanding of credit card transactions and customer insights while demonstrating effective data integration and visualization techniques suitable for intermediate users.
