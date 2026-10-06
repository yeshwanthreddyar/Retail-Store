# Retail Store Sales Analysis Dashboard

## 📊 Project Overview

**Retail Store Sales Analysis Dashboard** is an interactive **Microsoft
Power BI** business intelligence project designed to analyze retail
sales, profit, customers, products, stores, regions, channels, and
time-based performance.

The report combines a fact-based sales model with customer, product,
store, and calendar dimensions. It provides KPI cards, slicers, charts,
tables, and DAX-based time-intelligence analysis to help users
understand overall business performance and identify important sales and
profitability trends.

------------------------------------------------------------------------

## 🎯 Objectives

The main objectives of this project are to:

-   Monitor overall **sales and profit performance**.
-   Track **total orders, customers, and products**.
-   Analyze sales and profit across different **regions and cities**.
-   Compare performance across **product categories and brands**.
-   Analyze **online vs. offline sales channels**.
-   Examine customer-level sales performance.
-   Analyze store-level information and performance.
-   Perform **month, quarter, and year** comparisons.
-   Use DAX measures for **MTD, QTD, YTD, previous-period and percentage
    analysis**.
-   Provide an interactive dashboard for business decision-making.

------------------------------------------------------------------------

## 🛠️ Tools & Technologies

  -----------------------------------------------------------------------
  Tool / Technology                   Purpose
  ----------------------------------- -----------------------------------
  **Microsoft Power BI**              Dashboard development and
                                      visualization

  **Power Query**                     Data preparation and transformation

  **DAX**                             Measures, KPIs and analytical
                                      calculations

  **Power BI Data Model**             Relationships between fact and
                                      dimension tables

  **DAX Time Intelligence**           MTD, QTD, YTD and previous-period
                                      analysis
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 🗂️ Data Model

The project follows a dimensional / star-schema-style structure with the
following main tables:

### Fact Table

**Fact Sales**

Contains the transactional sales information used for analysis,
including measures and fields related to:

-   Sales
-   Profit
-   Quantity
-   Cost Price
-   Unit Price
-   Discount
-   Gross Sales
-   Discounted Amount
-   Store information
-   Customer information
-   Product information
-   Date

### Dimension Tables

**Dim Customer** - CustomerID - CustomerName - City - Region

**Dim Product** - ProductID - ProductName - Brand - Category

**Dim Store** - Store Key - StoreID - StoreName - Channel -
SalespersonID

**DIM CALENDAR** - Date - Month - Quarter - Year

### Model Structure

``` text
                 ┌─────────────────┐
                 │  Dim Customer   │
                 └────────┬────────┘
                          │
                          │
┌─────────────────┐       │       ┌─────────────────┐
│   Dim Product   │───────┼───────│   Dim Store     │
└─────────────────┘       │       └─────────────────┘
                          │
                   ┌──────▼───────┐
                   │  Fact Sales  │
                   └──────┬───────┘
                          │
                          │
                 ┌────────▼────────┐
                 │  DIM CALENDAR   │
                 └─────────────────┘
```

> The diagram represents the analytical model at a high level; the PBIX
> contains the actual Power BI relationships.

------------------------------------------------------------------------

## 📑 Report Pages

The PBIX contains **12 report pages**.

  -----------------------------------------------------------------------
  Page                                Purpose
  ----------------------------------- -----------------------------------
  **Overview**                        Main business dashboard containing
                                      KPIs, charts and interactive
                                      slicers

  **Page 1**                          Sales analysis using category,
                                      region, date and store-related
                                      fields

  **Page 2**                          Customer information and
                                      customer-level analysis

  **Page 3**                          Product information and
                                      product-level analysis

  **Page 4**                          Store information and store-related
                                      analysis

  **Page 5**                          Sales, profit and customer KPI
                                      analysis

  **Page 6**                          Detailed KPI and statistical
                                      analysis using min/max/average
                                      measures

  **Page 7**                          Brand-level sales analysis

  **Page 8**                          Regional/city/category percentage
                                      analysis

  **Page 9**                          MTD, QTD and YTD time-intelligence
                                      analysis

  **Page 10**                         Current vs previous
                                      month/quarter/year analysis

  **Time Series Analysis**            Time-based sales and profit trend
                                      analysis
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 📌 Key KPIs

The Overview page includes key performance indicators such as:

-   **Total Sales**
-   **Total Profit**
-   **Total Orders**
-   **Total Customers**
-   **Total Products**

These KPIs provide a quick summary of the overall retail business
performance.

------------------------------------------------------------------------

## 🎛️ Interactive Filters / Slicers

The report uses interactive slicers to allow users to drill into
specific portions of the data.

Common filters include:

-   **Region**
-   **City**
-   **Category**
-   **Brand**
-   **Month**
-   **Year**
-   **Channel**

The slicers dynamically update the relevant visuals and KPI values.

------------------------------------------------------------------------

## 📈 Visualizations

The dashboard contains multiple Power BI visual types, including:

-   KPI / Card visuals
-   Pie charts
-   Column charts
-   Bar charts
-   Line charts
-   Tables
-   Slicers
-   Text elements

### Example Analysis

The report can be used to analyze:

-   Sales by region
-   Profit contribution by region
-   Sales by brand and city
-   Quantity sold by product category
-   Online vs. offline sales
-   Top customers
-   Sales and profit trends over time
-   Regional sales percentages
-   City-level quantity percentages

------------------------------------------------------------------------

## 🧮 DAX & Measures

The project uses a variety of DAX measures for business calculations and
time intelligence.

### Core Measures

Examples include:

``` dax
Total Sales
Total Profit
Total Order
Total Customers
Total Products
```

### Sales & Profit Analysis

The model also contains measures for:

``` text
Total Gross Sales
Total Discounted Amount
Total Unit Price
Total Cost Price
Max Profit
Min Profit
Max Cost Price
Min Unit Price
Max Discount
Max Gross Sales
Min Gross Sales
Avg Gross Sales
Avg Discounted Amount
```

### Percentage Analysis

Measures include calculations for:

``` text
Total Sales (%)
Total Profit (%)
Total Sales Region (%)
Total Quantity(%) by City
```

These measures help determine the contribution of a region, city,
category, or other business segment to the overall result.

------------------------------------------------------------------------

## ⏱️ Time Intelligence

A major part of the project is the use of DAX time-intelligence
calculations.

The report includes:

### MTD --- Month to Date

Used to calculate performance from the beginning of the current month up
to the selected date.

Examples:

``` text
TOTALMTD
DATESMTD (SALES)
DATESMTD (PROFIT)
```

### QTD --- Quarter to Date

Used to measure performance from the beginning of the current quarter.

Examples:

``` text
TOTALQTD
DATESQTD (SALES)
DATESQTD (PROFIT)
```

### YTD --- Year to Date

Used to calculate cumulative performance from the beginning of the year.

Examples:

``` text
TOTALYTD
DATESYTD (sales)
DATESYTD (PROFIT)
```

### Previous Period Analysis

The report also contains measures for comparing current performance with
earlier periods:

``` text
PREVIOUS MONTH (PM)
PREVIOUS QUARTER (PQ)
PREVIOUS YEAR (PY)
PREVIOUS MONTH (PROFIT)
```

This enables month-over-month, quarter-over-quarter and year-over-year
style analysis.

------------------------------------------------------------------------

## 🔍 Business Questions Answered

The dashboard is designed to answer questions such as:

1.  What are the total sales and total profit?
2.  How many customers and products are available?
3.  Which region generates the highest sales?
4.  Which region contributes the most profit?
5.  Which brands perform best across cities?
6.  Which product categories generate the highest quantity sold?
7.  What percentage of sales comes from each region?
8.  What percentage of sales comes from online and offline channels?
9.  Who are the top customers?
10. How are sales and profit changing over time?
11. How does the current month compare with the previous month?
12. How does the current quarter compare with the previous quarter?
13. How does the current year compare with the previous year?
14. What are the minimum, maximum and average values for important sales
    metrics?

------------------------------------------------------------------------

## 📊 DAX Query Analysis

The PBIX also contains a DAX Query View file with analysis tasks
covering:

-   Customer details
-   Total customers
-   Maximum and minimum profit
-   Maximum cost price
-   Minimum unit price
-   Maximum discount
-   Total unit price
-   Total cost price
-   Online-channel profit
-   Quantity sold in a region
-   Average quantity sold in a city
-   Customers from a city
-   Average sales by city
-   Minimum/maximum profit by city
-   Filter-independent total profit calculations
-   Sales percentage by region
-   Profit percentage by category
-   Quantity percentage by city
-   Current month vs previous month profit
-   Current quarter vs previous quarter profit
-   Current month vs previous month quantity

------------------------------------------------------------------------

## 🧠 Skills Demonstrated

This project demonstrates practical knowledge of:

-   Power BI dashboard development
-   Data modeling
-   Star-schema concepts
-   Fact and dimension tables
-   Data visualization
-   KPI development
-   Slicers and interactive filtering
-   DAX measures
-   CALCULATE-based analysis
-   DIVIDE-based percentage calculations
-   Time-intelligence functions
-   MTD / QTD / YTD calculations
-   Previous-period comparison
-   Business intelligence reporting
-   Data storytelling

------------------------------------------------------------------------

## 🚀 How to Open the Project

### Prerequisites

Install:

-   **Microsoft Power BI Desktop**
-   A Windows environment capable of running Power BI Desktop

### Steps

1.  Download or clone this project.
2.  Open the `.pbix` file using **Power BI Desktop**.
3.  Wait for the report and data model to load.
4.  Navigate through the report pages using the page navigation.
5.  Use the slicers to filter the dashboard.
6.  Interact with charts and tables to explore the data.
7.  Open the **Model** view to inspect the relationships.
8.  Open the **Data** and **DAX Query** views to explore the analytical
    logic.

------------------------------------------------------------------------

## 📁 Project Structure

``` text
Retail-Store-PowerBI/
│
├── retailstore.pbix
└── README.md
```

------------------------------------------------------------------------

## 💡 Insights & Use Cases

This dashboard can be used by:

-   Retail business owners
-   Sales managers
-   Business analysts
-   Data analysts
-   Store managers
-   Management teams

It can support decisions related to:

-   Sales performance
-   Regional performance
-   Product strategy
-   Customer analysis
-   Store/channel performance
-   Profitability
-   Period-over-period performance

------------------------------------------------------------------------

## 🔮 Future Enhancements

Potential improvements include:

-   Adding a dedicated **profit margin %** KPI.
-   Adding automated refresh through Power BI Service.
-   Adding drill-through pages for customers, products and stores.
-   Adding tooltip pages for richer visual analysis.
-   Adding forecasting for future sales.
-   Adding year-over-year growth percentages.
-   Adding conditional formatting for positive/negative performance.
-   Adding a dedicated executive summary page.
-   Publishing the report to Power BI Service with role-level access.
-   Connecting the report to a live retail database.

------------------------------------------------------------------------

## 👨‍💻 Author

**Yeshwanth**

Power BI \| Data Analytics \| DAX \| Business Intelligence

------------------------------------------------------------------------

## ⭐ Project Summary

The **Retail Store Sales Analysis Dashboard** transforms transactional
retail data into an interactive analytical report. By combining
dimensional data modeling, DAX measures, time intelligence, KPIs and
interactive visualizations, the project provides a comprehensive view of
sales, profit, customers, products, stores, regions and time-based
performance.

This project is suitable for demonstrating practical **Power BI, DAX,
data modeling and business analytics skills** in an academic, portfolio
or interview setting.
