# E-commerce-_Sales-_Mini-Project<!-- ========================================================= -->
<!--                  E-COMMERCE SALES PROJECT                -->
<!-- ========================================================= -->

<div align="center">

# 🛒 E-commerce Sales Analysis

### Turning Raw Sales Data into Actionable Business Insights

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&duration=3000&pause=800&color=36BCF7&center=true&vCenter=true&width=750&lines=Data+Cleaning+with+Microsoft+Excel;Data+Transformation+with+Power+Query;Data+Modeling+and+DAX+in+Power+BI;Interactive+Sales+Analytics+Dashboard" alt="Animated project introduction" />

<br/>

![Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![Power Query](https://img.shields.io/badge/Power_Query-2F80ED?style=for-the-badge&logo=powerbi&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Analytics-blue?style=for-the-badge)
![Data Modeling](https://img.shields.io/badge/Data_Modeling-Star_Schema-6A5ACD?style=for-the-badge)

**An end-to-end data analytics project focused on sales performance, order trends, product categories, revenue, and geographical analysis.**

</div>

---

## 📌 Table of Contents

- [Executive Summary](#-executive-summary)
- [Business Problem](#-business-problem)
- [Project Objectives](#-project-objectives)
- [Technology Stack](#-technology-stack)
- [System Architecture](#-system-architecture--workflow)
- [Data Cleaning and Transformation](#-data-cleaning-and-transformation)
- [Data Modeling](#-data-modeling)
- [Dashboard Overview](#-dashboard-overview)
- [Key Performance Indicators](#-key-performance-indicators)
- [DAX Measures](#-key-dax-measures)
- [Business Insights](#-business-insights)
- [How to Run / View Project](#-how-to-run--view-project)
- [Skills Demonstrated](#-skills-demonstrated)
- [Future Enhancements](#-future-enhancements)

---

## 📊 Executive Summary

The **E-commerce Sales Analysis** project demonstrates an end-to-end data analytics workflow, from preparing raw transactional data to developing an interactive Power BI dashboard.

The project uses Microsoft Excel and Power Query to clean, standardize, and prepare sales data for analysis. The prepared dataset is then used in Power BI to build analytical visuals that help explore sales performance, order status, product categories, and geographical distribution.

From a Senior Data Analyst perspective, the primary objective is to convert raw transactional records into structured, decision-support information. The dashboard is designed to help business stakeholders understand sales performance, identify product and location trends, and monitor important business metrics.

### Project Deliverables

- Cleaned and standardized sales dataset.
- Data preparation and transformation workflow.
- Power BI analytical report with interactive visualizations.
- KPI calculations using DAX.
- Business-focused analysis of sales, orders, categories, and locations.

---

## 🎯 Business Problem

E-commerce businesses generate large volumes of transactional data containing order details, product categories, sales amounts, quantities, delivery information, and order statuses.

Analyzing this information directly from raw data can be difficult because of inconsistent formats, duplicate records, missing values, and the lack of a consolidated analytical view.

**Business objective:** Prepare reliable sales data and create an interactive dashboard that makes it easier to analyze sales performance, order trends, product categories, and geographical patterns.

### Key Business Questions

1. What is the total sales amount generated?
2. How many orders are recorded in the dataset?
3. Which product categories and sizes contribute to sales?
4. How do order statuses vary across the dataset?
5. Which cities or states have higher order quantities?
6. How can sales performance be monitored through interactive KPIs?

---

## 🎯 Project Objectives

- Clean and validate the source dataset before analysis.
- Handle duplicate records and missing values appropriately.
- Standardize date formats and text fields.
- Prepare data for reliable reporting.
- Create meaningful measures using DAX.
- Develop interactive Power BI report pages.
- Present business information in a clear, recruiter-friendly format.

---

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Microsoft Excel | Initial data inspection and cleaning |
| Power Query | Data transformation, duplicate removal, and missing-value handling |
| Power BI Desktop | Data modeling and interactive reporting |
| DAX | KPI calculations and analytical measures |
| GitHub | Project documentation and version control |

---

## ⚙️ System Architecture / Workflow

The project follows a structured data analytics pipeline.

```text
                 ┌────────────────────────┐
                 │   Raw E-commerce Data   │
                 │   Excel Workbook (.xlsx)│
                 └────────────┬───────────┘
                              │
                              ▼
                 ┌────────────────────────┐
                 │ Microsoft Excel        │
                 │ Data Inspection        │
                 │ Initial Data Cleaning  │
                 └────────────┬───────────┘
                              │
                              ▼
                 ┌────────────────────────┐
                 │ Power Query            │
                 │ Remove Duplicates      │
                 │ Handle Missing Values  │
                 │ Standardize Data Types │
                 └────────────┬───────────┘
                              │
                              ▼
                 ┌────────────────────────┐
                 │ Data Modeling          │
                 │ Fact & Dimension Tables│
                 │ Relationships          │
                 └────────────┬───────────┘
                              │
                              ▼
                 ┌────────────────────────┐
                 │ Power BI + DAX         │
                 │ KPI Calculations       │
                 │ Measures & Aggregations│
                 └────────────┬───────────┘
                              │
                              ▼
                 ┌────────────────────────┐
                 │ Interactive Dashboard  │
                 │ Sales | Orders         │
                 │ Categories | Locations │
                 └────────────────────────┘
```

---

## 🧹 Data Cleaning and Transformation

Data quality is a critical step because inaccurate or inconsistent data can lead to misleading business conclusions.

The following cleaning activities were part of the project workflow.

| Task | Description |
|---|---|
| Duplicate handling | Identify and remove duplicate records using appropriate business keys |
| Missing-value handling | Replace selected missing text values with `Unknown` |
| Amount handling | Replace selected missing amount values with `0`, where appropriate |
| Date formatting | Standardize date values for consistent analysis |
| Text standardization | Normalize city and state names |
| Numeric formatting | Format sales amounts consistently |
| Data validation | Check column types and values before reporting |

**Important:** Missing values replaced with zero must be interpreted carefully. A missing amount does not always mean that the actual sales amount was zero.

Duplicate removal should also be based on the intended record grain and business keys, rather than assuming that every repeated order ID is an accidental duplicate.

---

## 🏗️ Data Modeling

A star schema is a common analytical modeling approach that separates transactional facts from descriptive dimensions.

For a production-style version of this project, the model can be organized as follows.

**Note:** This is a proposed logical model. The diagram should be updated to match the actual tables and relationships implemented in the Power BI file.

### Star Schema Diagram

```text
                     ┌─────────────────────┐
                     │     DimDate         │
                     ├─────────────────────┤
                     │ PK: DateKey         │
                     │     FullDate        │
                     │     Month           │
                     │     Year            │
                     └──────────┬──────────┘
                                │ 1
                                │
                                │ *
┌─────────────────────┐         │         ┌─────────────────────┐
│    DimProduct       │         │         │    DimLocation      │
├─────────────────────┤         │         ├─────────────────────┤
│ PK: ProductKey      │         │         │ PK: LocationKey     │
│     SKU             │         │         │     ShipCity        │
│     Category        │         │         │     ShipState       │
│     Size            │         │         │     ShipCountry     │
└──────────┬──────────┘         │         └──────────┬──────────┘
           │ 1                  │                    │ 1
           │                    │                    │
           │ *                  │ *                  │ *
           └────────────────────┼────────────────────┘
                                │
                                ▼
                     ┌─────────────────────┐
                     │     FactSales       │
                     ├─────────────────────┤
                     │ PK: SalesKey*       │
                     │ FK: DateKey         │
                     │ FK: ProductKey      │
                     │ FK: LocationKey     │
                     │ OrderID             │
                     │ OrderStatus         │
                     │ Quantity            │
                     │ Amount               │
                     └─────────────────────┘

* SalesKey is a proposed surrogate key if one is needed.
```

### Modeling Principles

- **FactSales:** Stores transactional sales information and numeric values used for analysis.
- **DimDate:** Supports month-wise and year-wise reporting.
- **DimProduct:** Supports category, SKU, and size analysis.
- **DimLocation:** Supports city, state, and country analysis.
- **Primary keys (PK):** Uniquely identify dimension or fact records where applicable.
- **Foreign keys (FK):** Connect fact records to their associated dimensions.

### Relationship Design

- Use one-to-many relationships from dimensions to the fact table.
- Prefer single-direction filtering from dimensions to facts.
- Ensure dimension keys are unique.
- Define the fact table's grain before creating relationships.
- Use a dedicated date table for reliable time-based calculations.

**Implementation note:** If the current Power BI project uses a single flat table, retain that description until the model is actually split into fact and dimension tables. Do not claim a star schema is implemented unless it exists in the PBIX file.

---

## 📈 Dashboard Overview

The report is organized around the following analytical views.

### 1. Sales Overview

Provides a high-level view of sales performance using KPI cards and summary visuals.

Potential metrics:
- Total Sales Amount
- Total Orders
- Average Order Amount
- Total Quantity Sold

### 2. Order Analysis

Examines order distribution and operational patterns.

Potential analysis:
- Order status distribution
- Month-wise order trends
- Order counts by city
- Shipped, cancelled, and unshipped order analysis

### 3. Category Analysis

Explores product-level performance.

Potential analysis:
- Sales amount by category
- Quantity by size
- Average sales amount by category or size
- Product distribution across categories

### 4. Location Analysis

Explores the geographical distribution of orders.

Potential analysis:
- Order quantity by state
- Order counts by city
- Geographical sales distribution
- State-level comparisons

### 5. Revenue Analysis

Provides a focused view of monetary performance.

Potential analysis:
- Total sales amount
- Revenue trends over time
- Sales contribution by category
- Sales contribution by location

**Metric definition:** The `Amount` column represents the sales amount recorded in the source data. Confirm the treatment of cancellations, returns, discounts, and other adjustments before describing this metric as recognized revenue.

---

## 📌 Key Performance Indicators

| KPI | Business Purpose |
|---|---|
| Total Sales Amount | Measures the total recorded monetary value |
| Total Orders | Measures distinct order IDs |
| Total Quantity | Measures the recorded quantity |
| Average Order Amount | Shows the average amount per distinct order, when calculated at order level |
| Cancelled Orders | Helps monitor order cancellations |
| Sales by Category | Compares monetary performance across categories |

---

## 🧮 Key DAX Measures

The following are example measures based on the proposed `FactSales` table. Adjust table and column names to match the actual Power BI model.

### 1. Total Sales Amount

```dax
Total Sales =
SUM ( FactSales[Amount] )
```

**Purpose:** Calculates the sum of the sales amount in the current filter context.

### 2. Total Orders

```dax
Total Orders =
DISTINCTCOUNT ( FactSales[OrderID] )
```

**Purpose:** Counts distinct order IDs rather than counting every transaction row.

### 3. Total Quantity

```dax
Total Quantity =
SUM ( FactSales[Quantity] )
```

**Purpose:** Calculates the total recorded quantity.

### 4. Average Amount per Order

```dax
Average Order Amount =
DIVIDE (
    [Total Sales],
    [Total Orders],
    0
)
```

**Purpose:** Calculates average recorded sales amount per distinct order.

This is different from averaging the `Amount` column row by row. Use this measure when the intended business definition is sales amount divided by distinct orders.

### 5. Cancelled Orders

```dax
Cancelled Orders =
CALCULATE (
    DISTINCTCOUNT ( FactSales[OrderID] ),
    FactSales[OrderStatus] = "Cancelled"
)
```

**Purpose:** Counts distinct orders whose status is `Cancelled`.

Verify that the status column uses these exact values. If the dataset contains multiple status rows per order, define which status should represent the final order outcome.

### 6. Sales by Category

No additional measure is required if `Total Sales` already exists.

Use:
- **Axis:** `DimProduct[Category]`
- **Values:** `[Total Sales]`

Power BI automatically evaluates the measure for each category using the model relationships and filter context.

### 7. Year-to-Date Sales (Optional)

Use this measure only if the model includes a properly configured and marked date table.

```dax
YTD Sales =
TOTALYTD (
    [Total Sales],
    DimDate[FullDate]
)
```

**Purpose:** Calculates year-to-date sales based on the selected date context.

---

## 🔍 Business Insights

The final insights should be based on the actual dashboard results rather than assumptions.

Use the following template after validating your visuals.

### Insight 1: Sales Performance

- **Finding:** [Insert the actual total sales amount and the relevant comparison.]
- **Business interpretation:** Explain whether sales are increasing, decreasing, or concentrated in specific periods.

### Insight 2: Product Category Performance

- **Finding:** [Insert the highest-performing category and its sales amount or contribution.]
- **Business interpretation:** Explain which categories contribute most to recorded sales and may require further investigation.

### Insight 3: Geographical and Order Trends

- **Finding:** [Insert the state or city with the highest relevant order quantity, plus any important order-status pattern.]
- **Business interpretation:** Explain how the geographical distribution or order outcomes could inform operational planning.

**Validation checklist:**

- Confirm rankings from the report.
- Include actual numbers where available.
- Specify whether the metric is sales amount, order count, or quantity.
- Avoid claiming causation from descriptive charts alone.

---

## 🚀 How to Run / View Project

Follow these steps to review the project.

### Prerequisites

- Microsoft Excel
- Power BI Desktop
- The project Excel workbook
- The Power BI report file (`.pbix`)

### Step 1: Clone the Repository

Open a terminal and run:

```bash
git clone https://github.com/YOUR_USERNAME/E-commerce-Sales.git
cd E-commerce-Sales
```

Replace `YOUR_USERNAME` with your GitHub username.

### Step 2: Review the Source Data

Open the Excel workbook and inspect the source columns, data types, and cleaning steps.

### Step 3: Open the Power BI Report

Open the `.pbix` file using Power BI Desktop.

### Step 4: Refresh the Data

If Power BI requests a data source location, update the source path to match the location of the Excel workbook.

Select **Home → Refresh** to reload the data.

### Step 5: Explore the Dashboard

Navigate through the report pages and interact with:
- KPI cards
- Category charts
- Order-status visuals
- Location charts and maps
- Revenue and sales analysis

Use slicers and filters, if available, to investigate different segments of the data.

### Step 6: Review the Data Model

Open Model view in Power BI Desktop to inspect the table relationships and verify that the measures return the expected results.

---

## 📁 Suggested Repository Structure

```text
E-commerce-Sales/
│
├── README.md
├── Ecommerce_Sales_Analysis.xlsx
├── E-commerce-Sales.pbix
│
└── docs/
    └── data_dictionary.md
```

Keep only the files and folders that actually exist in the repository. Update the filenames above to match your uploaded project files.

If the workbook contains sensitive or restricted information, do not publish the raw dataset publicly.

---

## 💡 Skills Demonstrated

### Data Analytics
- Exploratory data analysis
- Data quality checks
- KPI definition
- Business-focused reporting
- Trend and category analysis

### Data Preparation
- Microsoft Excel
- Power Query transformations
- Missing-value handling
- Duplicate handling
- Data type and format standardization

### Business Intelligence
- Power BI report development
- DAX measures
- Data relationships
- Interactive visualizations
- Filter context and aggregations

### Documentation
- GitHub repository management
- Technical project documentation
- Business problem definition
- Analytical storytelling

---

## 🔮 Future Enhancements

- Add month-over-month and year-over-year sales comparisons.
- Implement a validated star schema with dedicated dimension tables.
- Add a data dictionary and documented KPI definitions.
- Create automated data quality checks.
- Analyze order cancellations and fulfillment performance.
- Add dynamic time-based measures and advanced DAX calculations.
- Improve report accessibility, navigation, and visual consistency.

---

## 👩‍💻 Author

Ramya.M

 Data Analyst |  Power BI Dashboard

Interested in transforming raw data into meaningful business insights through data cleaning, analytical modeling, and interactive reporting.

---





