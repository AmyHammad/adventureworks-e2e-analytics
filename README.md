# AdventureWorksLT2019 E2E Analytics – SQL, Power BI, Excel & Python

## 1. Project overview

This project is an end-to-end analytics case study based on the **AdventureWorksLT2019** sample database from Microsoft.  
I treat AdventureWorksLT as if I were a junior Data/Business Analyst in a real e-commerce / retail company, and answer stakeholder questions about:

- Sales performance over time
- Customers and regions
- Product and category performance
- Order behaviour (basket size, discounts, etc.)

I use multiple tools across the full workflow:

- **SQL Server (T-SQL)** – data exploration and business queries
- **Power BI** – interactive dashboards for stakeholders
- **Excel** – quick management reporting with pivot tables
- **Python (pandas)** – deeper analysis and experiments
- **Git & GitHub** – version control and documentation

---

## 2. Business scenario

**Company:** AdventureWorks Cycles – a fictional manufacturer and reseller of bicycles and related products.  
**Data:** Microsoft **AdventureWorksLT2019** sample database (OLTP, lightweight version).

As a junior Analyst, I was asked to build:

1. **Sales performance report**
   - How are we doing by year and month?
   - Which product categories and products drive most revenue?

2. **Customer & regional insights**
   - Which customers and cities are the most valuable?
   - How concentrated is our revenue (top customers vs the rest)?

3. **Order & discount analysis**
   - What is the typical order size and value?
   - How do discounts affect revenue?

4. **Executive dashboard**
   - A compact view (in Power BI and Excel) that managers can use to track KPIs.

---

## 3. Dataset and tables

AdventureWorksLT2019 stores most business data in the **SalesLT** schema.  
For this project I focus mainly on:

- **Sales & orders**
  - `SalesLT.SalesOrderHeader`
  - `SalesLT.SalesOrderDetail`
- **Customers & addresses**
  - `SalesLT.Customer`
  - `SalesLT.Address`
  - `SalesLT.CustomerAddress`
- **Products & categories**
  - `SalesLT.Product`
  - `SalesLT.ProductCategory`
  - `SalesLT.ProductModel`

> Note: The database is the standard Microsoft AdventureWorksLT2019 sample  
> (downloaded from Microsoft and restored in SQL Server).

A detailed **data dictionary** and **ERD sketch** are in `docs/`:

- `docs/data_dictionary.md`
- `docs/erd.png`

---

## 4. Tools & tech stack

- **Database:** SQL Server + SQL Server Management Studio (SSMS)
- **Query language:** T-SQL
- **BI & reporting:** Power BI Desktop, Excel
- **Programming:** Python (pandas, Jupyter / VS Code)
- **Version control:** Git & GitHub

---

## 5. Analysis questions

The project is structured around realistic business questions:

### 5.1 Sales performance

- What is total revenue per **year and month**?
- How is revenue evolving **over time**?
- Which **countries / cities** and **product categories** generate the most revenue?

### 5.2 Products & categories

- Which **product categories** are the most profitable?
- What are the **top 10 products** by revenue and by quantity sold?
- Are there **low-performing products** that might be candidates for discontinuation?

### 5.3 Customers & regions

- Who are our **top customers** by revenue?
- How concentrated is revenue (e.g. top 10 customers vs the rest)?
- Which **countries / cities** show the highest average order values?

### 5.4 Order behaviour & discounts

- What is the **average order value** and **average order size** (items per order)?
- How often are **discounts** used, and how much revenue do discounted items generate?
- Is there a difference in order value between **discounted** and **non-discounted** orders?

These questions are first explored with **SQL** and then visualised in **Power BI** and **Excel**.  
A separate **Python notebook** reproduces some of the analysis in pandas and explores additional insights.

---

## 6. Repository structure

```text
adventureworkslt-e2e-analytics/
  README.md
  data/
    raw/           # (optional) CSV exports from SQL
    processed/     # (optional) cleaned/aggregated data
  sql/
    01_setup_and_checks.sql
    02_sales_performance.sql
    03_products_and_categories.sql
    04_customers_and_regions.sql
    05_order_behaviour_and_discounts.sql
  powerbi/
    AdventureWorksLT_Sales_Dashboard.pbix
  excel/
    AdventureWorksLT_Sales_Dashboard.xlsx
  python/
    adventureworkslt_sales_analysis.ipynb
  docs/
    data_dictionary.md
    erd.png
  images/
    powerbi_overview.png
    powerbi_customers.png
    powerbi_products.png
