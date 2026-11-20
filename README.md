# Business Insights 360 | AtliQ Hardware
## 1. Project Overview

Business Insights 360 is an end-to-end Business Intelligence project developed for **AtliQ Hardware**, a fictional consumer electronics company operating across multiple markets and sales channels.

The project focuses on transforming business data into meaningful insights through interactive Power BI dashboards. It provides a consolidated view of financial performance, sales trends, market performance, customer behavior, and supply chain operations.

The objective is to support data-driven decision-making by helping stakeholders monitor key performance indicators, identify business trends, and evaluate operational performance.

### Live Power BI Report

[View Live Power BI Dashboard](https://app.powerbi.com/view?r=eyJrIjoiZWQ2YTQzNjQtYjIyZi00N2E3LTgzNTQtMDEzYTc2NzlkZDE0IiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)

## 2. Business Problem

AtliQ Hardware experienced challenges in making effective business decisions using traditional reporting methods and fragmented Excel-based analysis.

As the company expanded into new markets, management needed a centralized analytics solution to understand business performance and identify areas requiring improvement.

One major setback occurred when the company expanded into the American market based primarily on surveys, business intuition, and Excel-based analysis, resulting in an unexpected loss.

The key challenges included:

- Limited visibility into overall financial performance.
- Difficulty tracking sales and profitability across markets.
- Lack of consolidated customer and product performance analysis.
- Challenges in comparing actual sales with forecasts.
- Limited visibility into supply chain performance.
- Time-consuming manual reporting processes.
- Difficulty making timely, data-driven business decisions.

### Business Goals

The project aims to help the company:

- Improve data-driven decision-making.
- Monitor financial and sales performance.
- Identify high-performing and underperforming markets.
- Understand customer and product contributions.
- Improve visibility into profitability.
- Compare forecast demand with actual sales.
- Support inventory and supply chain planning.
- Provide stakeholders with a consolidated reporting solution.

## 3. Project Objectives

- Develop an interactive Business Intelligence dashboard.
- Analyze revenue, net sales, gross margin, and profitability.
- Evaluate customer and product performance.
- Compare actual sales with forecast quantities.
- Monitor supply chain performance and forecast accuracy.
- Provide actionable insights through interactive visualizations.
- Enable management to make informed business decisions.
- Apply data modeling, ETL, DAX, and reporting best practices.

## 4. Stakeholder Requirements & Project Planning

A successful Business Intelligence project begins with understanding the business problem and stakeholder expectations.

Before dashboard development, the following areas need to be considered:

| Area | Key Questions |
|---|---|
| Business Objectives | What business problem should the dashboard solve? |
| Stakeholders | Who will use the dashboard, and what information do they need? |
| KPIs | Which business metrics are important for decision-making? |
| Data Requirements | Where is the data stored, and how frequently is it updated? |
| Project Planning | What are the deadlines, milestones, and deliverables? |
| Data Quality | Are there missing values, inconsistencies, or data-quality issues? |
| Dashboard Design | What layout, navigation, and filtering options are required? |
| Project Risks | What technical or business challenges could affect delivery? |

This requirement-first approach ensures that the dashboard is designed around business needs rather than just visual presentation.

## 5. Dashboard Modules

The Power BI report contains six main pages.

| Dashboard Page | Purpose |
|---|---|
| Home | Central navigation page for the report |
| P&L Check | Financial performance validation and analysis |
| Finance View | Revenue, expenses, gross margin, and profitability analysis |
| Supply Chain View | Forecast performance, supply chain metrics, and operational analysis |
| Sales View | Sales performance across customers, products, and markets |
| Market View | Geographic and market-level business performance |

## 6. Technology Stack

| Technology | Purpose |
|---|---|
| Power BI Desktop | Dashboard development and visualization |
| MySQL / SQL | Source database and data extraction |
| Power Query / M | Data cleaning, transformation, and ETL |
| DAX | Measures, KPIs, and business calculations |
| Microsoft Excel | Supporting data analysis and validation |
| DAX Studio | DAX analysis and performance optimization |
| Power BI Service | Report publishing, sharing, and refresh management |
| Git & GitHub | Version control and project documentation |
| Git LFS | Managing large Power BI project files |

## 7. Data Sources & Dataset Understanding

The project documentation identifies the following MySQL databases:

- `gdb041`
- `gdb056`

These databases provide the business data used for analysis.

The model includes sales, forecast, customer, product, market, financial, and operational information.

### Business Dimensions

According to the project dataset documentation:

| Business Dimension | Dataset Information |
|---|---|
| Customers | 75 distinct customers |
| Markets | 27 distinct markets |
| Sub-zones | 7 |
| Regions | 4 |
| Platforms | Brick & Motors and E-commerce |
| Sales Channels | Retailer, Direct, Distributor |

### Regions

- APAC
- EU
- LATAM
- NA

### Sales Channels

1. Retailer
2. Direct
3. Distributor

### Platforms

- **Brick & Motors:** Physical and offline sales platforms.
- **E-commerce:** Online platforms, including examples such as Amazon and Flipkart in the project notes.

### Product Categories

The dataset documentation describes approximately 14 product categories, including examples such as Internal HDD and Keyboard.

The product information also includes divisions, segments, categories, products, and variants.

## 8. Data Model

The Power BI model contains dimension tables, fact tables, supporting calculation tables, and measures.

### Dimension Tables

- `dim_date` – Date and fiscal calendar information.
- `dim_customer` – Customer, platform, and sales channel information.
- `dim_market` – Market, sub-zone, and regional information.
- `dim_product` – Product, division, segment, category, and variant information.
- `fiscal_year` – Fiscal year reference information.

### Fact Tables

- `fact_sales_monthly` – Monthly sales quantity information.
- `fact_forecast_monthly` – Monthly forecast quantity information.
- `fact_actuals_estimates` – Financial and operational actuals and estimates.

### Supporting Tables

The model also includes supporting tables for:

- Gross price
- Manufacturing cost
- Freight cost
- Pre-invoice deductions
- Post-invoice deductions
- Operational expenses
- Remaining forecast
- Key measures and P&L calculations

### Data Modeling Approach

The project documentation describes a **Snowflake Data Model**.

Data modeling is important because it forms the foundation of the entire Power BI report. Relationships between fact and dimension tables influence calculations, filters, and visual interactions.

Important modeling considerations include:

- Understanding the grain of each fact table.
- Identifying key columns and relationships.
- Maintaining a consistent date dimension.
- Avoiding unnecessary columns in the model.
- Ensuring appropriate filter propagation.
- Creating reusable measures.
- Validating calculations across different filter selections.

### Data Model Diagram

Add your actual Power BI model screenshot here:

```text
Documentation/Data_Model.png
```

## 9. Data Preparation & ETL Workflow

The project follows an end-to-end data analytics workflow.

### Data Flow

```text
MySQL Databases
       |
       v
Power BI Data Connection
       |
       v
Power Query / M
       |
       v
Data Cleaning & Transformation
       |
       v
Data Modeling
       |
       v
DAX Measures & KPIs
       |
       v
Interactive Dashboards
       |
       v
Data Validation & Optimization
       |
       v
Business Insights
```

### Data Transformation Techniques

- Connecting Power BI to MySQL databases.
- Exploring source tables and columns.
- Cleaning and transforming data using Power Query.
- Creating calculated columns where required.
- Creating reusable DAX measures.
- Establishing relationships between tables.
- Creating a date table using Power Query M.
- Performing data validation.
- Preparing data for analytical reporting.

## 10. Key Business Metrics

The report uses DAX measures to calculate important business KPIs.

### Financial Metrics

- Gross Sales
- Net Invoice Sales
- Pre-Invoice Deductions
- Post-Invoice Deductions
- Net Sales
- Manufacturing Cost
- Freight Cost
- Total Cost of Goods Sold
- Gross Margin
- Gross Margin Percentage
- Operational Expenses
- Net Profit
- Net Profit Percentage

### Sales Metrics

- Sales Quantity
- Net Sales
- Gross Margin
- Gross Margin per Unit
- Year-over-Year Change
- Year-over-Year Growth Percentage

### Supply Chain Metrics

- Forecast Quantity
- Sales Quantity
- Net Error
- Net Error Percentage
- Absolute Error
- Absolute Error Percentage
- Forecast Accuracy
- Forecast Accuracy Comparison

## 11. Selected DAX Measures

The following examples illustrate calculations used in the Power BI model.

### 1. Net Sales

```dax
NS $ =
SUM(fact_actuals_estimates[net_sales_amount])
```

### 2. Gross Margin

```dax
GM $ =
[NS $] - 'Key Measures'[Total COGS $]
```

### 3. Gross Margin Percentage

```dax
GM % =
DIVIDE([GM $], [NS $], 0)
```

### 4. Net Profit

```dax
Net Profit $ =
[GM $] + [Operational Expense $]
```

### 5. Net Profit Percentage

```dax
Net Profit % =
DIVIDE([Net Profit $], [NS $], 0)
```

### 6. Net Forecast Error

```dax
Net Error =
[Forecast Qty] - 'Key Measures'[Sales Qty]
```

### 7. Forecast Accuracy

```dax
Forecast Accuracy % =
IF(
    'Key Measures'[ABS Error %] <> BLANK(),
    1 - 'Key Measures'[ABS Error %],
    BLANK()
)
```

## 12. Financial Performance Analysis

The project covers the relationship between revenue, deductions, costs, and profitability.

### Financial Calculation Flow

```text
Gross Sales
     |
     v
Pre-Invoice Deductions
     |
     v
Net Invoice Sales
     |
     v
Post-Invoice Deductions
     |
     v
Net Sales
     |
     v
Cost of Goods Sold
     |
     v
Gross Margin
     |
     v
Operational Expenses
     |
     v
Net Profit
```

This analysis helps stakeholders understand how revenue deductions, manufacturing costs, freight costs, other costs, and operational expenses influence profitability.

### Key Financial Questions

- How is Net Sales performing?
- What is the Gross Margin percentage?
- How do deductions affect net revenue?
- How does Cost of Goods Sold influence profitability?
- What is the impact of operational expenses on Net Profit?
- How does financial performance change across fiscal periods?

## 13. Sales & Market Performance Analysis

The report supports analysis across multiple business dimensions.

### Sales Analysis

- Customer-level performance.
- Product-level performance.
- Sales by division and category.
- Channel-wise performance.
- Sales trends across time periods.
- Identification of high-performing and underperforming areas.

### Market Analysis

- Market-level performance.
- Regional comparisons.
- Sub-zone analysis.
- Customer distribution across markets.
- Geographic performance comparisons.

These dimensions help stakeholders investigate where sales are generated and which areas may require further attention.

## 14. Forecasting & Supply Chain Analysis

One important aspect of this project is the comparison between forecast demand and actual sold quantity.

The `fact_forecast_monthly` table contains forecast quantities expected from customers, while `fact_sales_monthly` contains actual sold quantities.

### Why Forecast Analysis Matters

Forecasting can support:

- Customer demand planning.
- Inventory planning.
- Warehouse optimization.
- Reduction of unnecessary storage costs.
- Product availability planning.
- Better supply chain decisions.

### Important Supply Chain KPIs

- Forecast Quantity
- Actual Sold Quantity
- Net Error
- Net Error Percentage
- Absolute Error
- Absolute Error Percentage
- Forecast Accuracy

Comparing forecast and actual quantities helps identify demand variances and areas where forecasting performance may need improvement.

## 15. Business Analysis

The dashboard is designed to help stakeholders investigate questions such as:

### Finance

- How is the company performing financially?
- What are the trends in Net Sales and Gross Margin?
- How do operational costs affect profitability?

### Sales

- Which customers and products contribute to sales?
- How does sales performance vary across markets?
- Which channels contribute to business performance?

### Market

- Which regions and markets have stronger sales performance?
- How does performance vary across geographic areas?
- Which markets require further investigation?

### Supply Chain

- How closely do actual sales match forecast quantities?
- Where are forecast errors occurring?
- How can forecast information support inventory planning?

The interactive report allows users to explore business performance using available filters and report visualizations.

## 16. Interactive Dashboard Features

The project includes Power BI concepts and techniques for building an interactive reporting experience.

### Dashboard Design

- Mockup-based dashboard development.
- Consistent visual layout.
- KPI indicators.
- Conditional formatting.
- Icons and background formatting.

### Navigation & Interactivity

- Bookmarks to switch between visuals.
- Page navigation using buttons.
- Dynamic titles based on applied filters.
- Interactive filters and slicers.
- Filter-based analysis.

These features improve report usability and help stakeholders explore information according to their requirements.

## 17. Data Validation & Quality Checks

Data validation is essential for maintaining the accuracy and reliability of a Business Intelligence report.

Important validation checks include:

- Comparing source database totals with Power BI totals.
- Checking sales and forecast quantities.
- Validating financial calculations.
- Checking date and fiscal-year filters.
- Testing customer, product, and market filters.
- Verifying calculations under different slicer selections.
- Checking for missing or inconsistent data.

The purpose is to ensure that the report provides consistent and reliable information for analysis.

## 18. Power BI Service & Deployment

Developing a dashboard is only one part of a Business Intelligence solution. Publishing, sharing, and maintaining reports are also important.

The project learning process covers:

- Publishing reports to Power BI Service.
- Creating Power BI Apps.
- Workspace management.
- Collaboration.
- Access permissions.
- Setting up a personal gateway.
- Configuring automatic data refresh.

These concepts provide an introduction to managing and sharing BI reports beyond Power BI Desktop.

## 19. Performance Optimization

A well-designed dashboard should provide accurate information while remaining responsive.

The project includes learning and applying:

- DAX Studio for DAX analysis.
- DAX measure optimization.
- Data-modeling best practices.
- Improving report performance.
- Reducing unnecessary model complexity.

Performance optimization is important because inefficient models and calculations can affect report responsiveness and usability.

## 20. Business Value of the Solution

The intended business value of Business Insights 360 is to provide a consolidated reporting environment for different business functions.

| Business Function | Potential Business Value |
|---|---|
| Finance | Better visibility into revenue, deductions, costs, and profitability |
| Sales | Easier analysis of customer, product, and market performance |
| Marketing | Better visibility into customer segments and market performance |
| Supply Chain | Improved understanding of forecast variance and demand patterns |
| Executive Management | Consolidated view of key business performance indicators |

These are intended analytical benefits of the reporting solution, not independently measured business results.

## 21. Skills Demonstrated

Through this project, I applied and developed skills in:

### Technical Skills

- SQL and MySQL
- Power BI Desktop
- Power Query and M
- DAX calculations and measures
- Data modeling
- DAX Studio
- Power BI Service
- Git and GitHub LFS

### Analytical Skills

- Business requirement analysis
- KPI development
- Financial analysis
- Sales performance analysis
- Customer and market analysis
- Forecast accuracy analysis
- Data validation
- Business reporting

### Business Intelligence Skills

- Data extraction and transformation
- ETL processes
- Interactive dashboard design
- Data storytelling
- Performance optimization
- Report publishing and maintenance

## 22. Repository Structure

```text
Business-Insights-360-Power-BI/
│
├── README.md
│
├── Dashboard/
│   └── Dashboard_Screenshots/
│       ├── Home.png
│       ├── P&L_Check.png
│       ├── Finance_View.png
│       ├── Supply_Chain_View.png
│       ├── Sales_View.png
│       └── Market_View.png
│
├── Project Files/
│   └── AM.pbix
│
├── Documentation/
│   ├── Data_Model.md
│   ├── DAX_Measures.md
│   └── Business_Insights.md
│
├── .gitattributes
└── LICENSE
```

Replace the example screenshot names with genuine screenshots exported from your final PBIX report.

## 23. How to Use This Project

1. Clone or download this repository.
2. Install Microsoft Power BI Desktop.
3. Open the `.pbix` file.
4. Configure the required database connection and credentials if prompted.
5. Refresh the data, if the original source databases are accessible.
6. Explore the report pages, interactive filters, and visualizations.

### Database Access Note

The project documentation identifies MySQL databases `gdb041` and `gdb056` as the data sources.

Database access, valid credentials, and compatible connection settings may be required to refresh or recreate the report. The repository does not necessarily contain the original source databases.

## 24. GitHub Large File Management

Power BI files can be large. Git Large File Storage (Git LFS) can be used to manage large `.pbix` files.

### Example Git LFS Commands

```bash
git lfs install
git lfs track "*.pbix"
git add .gitattributes
git add .
git commit -m "Add Business Insights 360 Power BI project"
git push
```

Do not commit database passwords, private credentials, confidential source data, or other sensitive information.

## 25. Project Outcome

This project demonstrates how business data can be transformed into an interactive analytical solution using Power BI.

It brings financial, sales, market, and supply chain analysis together in one reporting environment, helping stakeholders explore KPIs and understand business performance.

The project also provides practical experience in the complete Business Intelligence workflow, from understanding business requirements and preparing data to modeling, DAX development, dashboard design, validation, optimization, and publishing.

## 26. Acknowledgement

This project was developed as a Business Intelligence portfolio project by following the **Codebasics Power BI course** and the AtliQ Hardware case study.

The project demonstrates practical applications of Power BI, SQL, Power Query, DAX, data modeling, and business analytics.

---

**Tools:** Power BI | MySQL | SQL | Power Query | DAX | Excel | DAX Studio | Power BI Service | GitHub LFS

**Project Category:** Business Intelligence & Data Analytics
