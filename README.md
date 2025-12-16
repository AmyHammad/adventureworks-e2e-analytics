# AdventureWorks E2E Analytics – SQL, Power BI, Excel & Python

## 1. Project overview

This project is an end-to-end analytics case study based on the **AdventureWorks** sample database from Microsoft.  
I treat AdventureWorks as if I were a junior Data/Business Analyst in a real company, and answer stakeholder questions about:

- Sales performance
- Customers and territories
- Product performance
- Sales pipeline and sales reps

I use multiple tools across the full workflow:

- **SQL Server (T-SQL)** – data exploration and business queries
- **Power BI** – interactive dashboards for stakeholders
- **Excel** – quick management reporting with pivot tables
- **Python (pandas)** – deeper analysis and experiments
- **Git & GitHub** – version control and documentation

---

## 2. Business scenario

**Company:** AdventureWorks Cycles – a fictional manufacturer and reseller of bicycles and related products.  
**Data:** Microsoft AdventureWorks sample database (OLTP version).

As a junior Analyst, I was asked to build:

1. **Sales performance report**
   - How are we doing by year, quarter, and territory?
   - Which products and categories drive most revenue and profit?

2. **Customer & territory insights**
   - Which customer segments and regions are the most valuable?
   - How concentrated is our revenue in a few customers?

3. **Sales operations**
   - How are individual sales people and teams performing?
   - Are we meeting order quantity and revenue targets?

4. **Executive dashboard**
   - A compact view (in Power BI and Excel) that managers can use to track KPIs.

---

## 3. Dataset and tables

AdventureWorks includes many schemas. For this project I focus mainly on:

- **Sales schema**
  - `Sales.SalesOrderHeader`
  - `Sales.SalesOrderDetail`
  - `Sales.Customer`
  - `Sales.SalesPerson`
  - `Sales.SalesTerritory`
- **Production schema**
  - `Production.Product`
  - `Production.ProductSubcategory`
  - `Production.ProductCategory`
- **Person & geography**
  - `Person.Person`
  - `Person.Address`
  - `Person.StateProvince`
  - `Person.CountryRegion`

> Note: The database is the standard Microsoft AdventureWorks sample  
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

The project is structured around real-life business questions:

### 5.1 Sales performance

- What is total revenue per **year and quarter**?
- Which **sales territories** generate the most revenue and profit?
- How is revenue evolving **over time** (monthly trend)?

### 5.2 Products & categories

- Which **product categories and subcategories** are the most profitable?
- What are the **top 10 products** by revenue and by quantity sold?
- Are there **low-performing products** that might be candidates for discontinuation?

### 5.3 Customers & territories

- Who are our **top customers** by revenue?
- How concentrated is revenue (e.g. top 10 customers vs the rest)?
- Which **countries / regions** show the highest average order values?

### 5.4 Sales people & teams

- Who are the **top-performing sales people** by revenue and margin?
- How do sales people perform relative to their **sales quotas**?
- Which territories have the most **successful sales reps**?

These questions are first explored with **SQL** and then visualised in **Power BI** and **Excel**.  
A separate **Python notebook** reproduces some of the analysis in pandas and explores additional insights.

---

## 6. Repository structure

```
