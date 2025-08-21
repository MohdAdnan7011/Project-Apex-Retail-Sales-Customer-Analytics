# Project-Apex-Retail-Sales-Customer-Analytics in PowerBI

## Project Overview

This project presents a comprehensive analysis of a retail sales dataset, designed to uncover key business insights and demonstrate a full-cycle data analysis workflow. The primary goal was to transform raw sales data into an interactive, two-part business intelligence report that empowers stakeholders to make data-driven decisions.

The entire project, from data cleaning and modeling to the final interactive dashboards, was completed using **Microsoft Power BI** and its integrated tools (Power Query and DAX).

---

## Dashboards 📊

### 1. Sales Velocity Monitor (Executive Summary)

This dashboard provides a high-level, at-a-glance overview of the company's sales performance. It is designed for executives and managers who need a quick pulse on the business's health.


**Key Questions Answered:**
* What are our total sales, orders, and average order value (AOV)?
* How are sales trending over time?
* Which countries and product lines are the top performers?
* What is the operational status of our orders?

---

### 2. Customer & Product Deep Dive

This dashboard is designed for sales and marketing managers, offering a granular look at customer behavior and product performance to identify strategic opportunities.


**Key Insights & Features:**
* **Top 10 Customers:** Identifies the most valuable customers by total sales, enabling focused account management.
* **Product Portfolio Analysis:** A scatter plot visualizes the relationship between product price and sales volume, helping to categorize products.
* **Deal Size Mix:** A matrix breaks down sales by product line and deal size (Small, Medium, Large), revealing which products contribute to high-value deals.
* **YoY Sales Growth:** A combination chart tracks monthly sales against the year-over-year growth percentage, providing crucial context on business momentum.

---

## Data Cleaning & Preparation (Power Query)

Before analysis, the raw data required significant cleaning and transformation. The following steps were performed in Power Query:

* **Data Type Correction:** Ensured all columns were in the correct format (e.g., `ORDERDATE` converted from Text to Date using Locale).
* **Handling Missing Values:** Filled `null` values in `STATE` and `POSTALCODE` by creating a lookup table from existing valid data and merging queries.
* **Column Creation & Transformation:**
    * Concatenated `CONTACTFIRSTNAME` and `CONTACTLASTNAME` into a `ContactFullName` column.
    * Created a `Cleaned Phone` column by stripping non-numeric characters and enforcing a 10-digit length rule, setting others to null.

---

## Data Modeling & DAX

A robust data model was created to support time-based analysis and complex calculations.

* **Date Table:** A dynamic calendar table was created using the `CALENDARAUTO()` DAX function. This table was marked as the official date table and was used for all time-based visuals and calculations.
* **Relationships:** A one-to-many relationship was established between the `Date Table` and the `sales_data` table.
* **DAX Measures:** Several key measures were written to power the visuals, including:
    * `Total Sales`, `Total Orders`, `AOV`
    * An advanced **`YoY Sales Growth %`** measure using `SAMEPERIODLASTYEAR` to provide critical business context.

---

## Skills & Tools Demonstrated

* **ETL:** Data cleaning, transformation, and enrichment using **Power Query**.
* **Data Modeling:** Creation of a star schema with a dedicated Date Table.
* **DAX:** Writing basic and advanced measures for complex calculations.
* **Data Visualization:** Choosing appropriate visuals to answer specific business questions.
* **Business Acumen:** Identifying key performance indicators (KPIs) and deriving actionable insights from the data.
* **Tools:** Microsoft Power BI, Power Query, DAX.

---

