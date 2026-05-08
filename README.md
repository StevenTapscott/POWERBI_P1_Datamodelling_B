#  Sales Input & Reporting System (Power BI)

##  Overview  
This project demonstrates the development of an end-to-end business intelligence solution using Power BI. A structured sales dataset was created and transformed into an interactive dashboard to support reporting and performance analysis.

---

##  Objectives  
- Develop a structured dataset for sales analysis  
- Connect and transform data within Power BI
- Developed a star schema
- Build an interactive dashboard to monitor sales performance  
- Deliver insights to support data-driven decision-making  

---

##  Tools & Technologies  
- Power BI  
- Power Query  
- Data Modelling (basic relationships)  
- Data Visualisation  

---

##  Data Source  
- Custom-built sales dataset  
- Includes:
  - Sales records  
  - Product information  
  - Transaction-level data  

---

##  Key Steps  

### 1. Data Preparation  
- Imported dataset into Power BI  
- Cleaned and transformed data using Power Query  
- Ensured correct data types and structure  

### 2. Data Modelling  
- Established relationships between tables  
- Created a clean and logical schema for reporting  

### 3. Dashboard Development  
- Built visuals including:
  - KPI cards (Total Sales, Transactions)  
  - Sales trends over time  
  - Product performance analysis  

---
##  Key DAX Measures

- Total Sales = SUM(Sales[SalesAmount])  
- Total Transactions = DISCTINCTCOUNT(Sales[OrderID])  
- Average Order Value = Total Sales ÷ Total Orders  
- Sales YTD = Year-to-date sales using time intelligence functions
- DateTable = 
ADDCOLUMNS(
    CALENDAR(MIN(Sales[Order Date]), MAX(Sales[Order Date])),
    "Year", YEAR([Date]),
    "Month", FORMAT([Date], "MMM"),
    "MonthNumber", MONTH([Date])
)
- Selected Year (Title) = IF(
    HASONEVALUE(DateTable[Year]),
    "ST Projects: Sales Overview - " & VALUES(DateTable[Year]),
    "ST Projects: Sales Overview - All Years"
)
These measures were used to power KPI cards and trend analysis within the dashboard.
##  Key Insights  
- Identified top-performing products  
- Analysed sales trends across time periods  
- Highlighted underperforming areas  

---

##  Business Value  
- Demonstrates a complete analytics workflow (data → insights → dashboard)  
- Enables clear visibility of sales performance  
- Supports better decision-making through interactive reporting  

---

##  Challenges Faced  
- Structuring data for effective modelling  
- Designing clear and intuitive dashboard layouts  
- Ensuring consistency across visuals and metrics  

---

##  Outcome  
Successfully developed a fully functional Power BI dashboard, showcasing the ability to transform raw data into meaningful insights through effective data modelling and visualisation.
