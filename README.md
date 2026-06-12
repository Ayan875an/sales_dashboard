# 📊 Sales Performance Dashboard | Business Review (2015–2018)

<img width="983" height="555" alt="Screenshot 2026-06-12 203354 - Copy" src="https://github.com/user-attachments/assets/21c72ef3-01ae-4bc5-8906-3784c46612b3" />



# 📊 Sales Performance Dashboard | Business Review (2015–2018)

![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Measures-blue)
![Excel](https://img.shields.io/badge/Data-Analysis-green)
![Status](https://img.shields.io/badge/Project-Completed-success)

---

# 📌 Project Overview

This Power BI dashboard provides a comprehensive analysis of business performance from **2015 to 2018**. The project focuses on sales growth, profitability, target achievement, regional performance, category analysis, return rates, and delivery delays.

The dashboard enables stakeholders to monitor key business metrics, evaluate regional manager performance, identify operational risks, and make data-driven decisions.

---

# 🎯 Business Objectives

The dashboard was designed to answer the following business questions:

- How is the business performing overall?
- Which regions contribute the highest sales and profit?
- Which Regional Managers are driving performance?
- Are category sales targets being achieved?
- How have sales and profits changed over time?
- Which categories have the highest returns?
- How do delivery delays impact operations?
- What business risks require attention?

---

# 📂 Dataset Description

The dataset represents a retail company's sales operations from **2015 to 2018** and contains information related to orders, customers, product categories, sales targets, returns, and regional management.

The data was used to analyze business performance, profitability, operational efficiency, and target achievement across different regions and categories.

---

## Dataset Tables

### Orders Table

The primary fact table containing transactional sales records.

**Key Fields**
- Order ID
- Order Date
- Customer ID
- Customer Name
- City
- Country
- Region
- Category
- Sales
- Profit
- Discount
- Delivery Days
- Returned Status
- Delayed Status

**Purpose**

Used to calculate:
- Total Sales
- Total Profit
- Total Orders
- Profit Margin
- Delay Rate
- Category Performance

---

### People Table

Contains information about Regional Managers assigned to each region.

**Key Fields**
- Region
- Regional Manager

**Purpose**

Used for:
- Regional Performance Analysis
- Manager Performance Tracking
- Manager Ranking

---

### Target Table

Contains category-wise sales targets.

**Key Fields**
- Year
- Category
- Sales Target

**Purpose**

Used to:
- Compare Actual Sales vs Target
- Calculate Achievement Percentage
- Identify Target Gaps

---

### Returns_Bridge Table

Bridge table connecting returned orders with the Orders table.

**Purpose**

Used to:
- Maintain relationships
- Improve return analysis

---

### Returns_Detail Table

Contains returned order records.

**Purpose**

Used to:
- Calculate Return Rate %
- Analyze returned orders

---

# 📊 Dataset Summary

| Attribute | Value |
|------------|---------|
| Time Period | 2015 – 2018 |
| Industry | Retail |
| Fact Table | Orders |
| Dimension Tables | People, Target |
| Supporting Tables | Returns_Bridge, Returns_Detail |
| Regions | Central, North, South |
| Categories | Furniture, Office Supplies, Technology |
| Reporting Tool | Power BI |

---

# 🏗️ Data Model

The dashboard follows a **Fact-Dimension Model** to ensure efficient reporting and filtering.

### Fact Table
- Orders

### Dimension Tables
- People
- Target

### Supporting Tables
- Returns_Bridge
- Returns_Detail

---

## Data Model Diagram

![Data Model](screenshots/data_model.png)

---

## Relationships

| From Table | To Table | Relationship |
|------------|-----------|-------------|
| Orders | People | Many-to-One |
| Orders | Target | Many-to-One |
| Orders | Returns_Bridge | One-to-Many |
| Returns_Bridge | Returns_Detail | One-to-One |

---

# 🛠️ Tools & Technologies

- Power BI Desktop
- Power Query
- DAX
- Excel
- Data Modeling
- Data Visualization

---

# 📈 Dashboard Pages

The report consists of **4 interactive dashboard pages**.

---

# 1️⃣ Executive Business Overview

## Purpose

Provide a high-level summary of business performance.

### KPIs

| Metric | Value |
|----------|----------|
| Total Sales | 2.94M |
| Total Orders | 5K |
| Total Profit | 372.83K |
| Return Rate | 6.37% |
| Delay Rate | 40.76% |
| Profit Margin | 12.69% |

### Visualizations

- Sales & Profit by Year
- Sales by Region
- Year-over-Year Comparison
- KPI Cards
- Year Slicer

### Key Insights

- Sales increased consistently from 2015 to 2018.
- 2018 generated the highest revenue and profit.
- Central region contributed the largest share of sales.
- Business maintained a positive profit trend.

---

## Dashboard Preview

![Executive Overview](screenshots/executive_overview.png)

---

# 2️⃣ Regional Manager Performance

## Purpose

Evaluate sales and profit performance of Regional Managers.

### Managers Covered

- Emily Burns
- Ross DeVincentis
- Damala Kotsonis

### Visualizations

- Manager KPI Cards
- Manager Ranking
- Sales Trend by Manager
- Manager × Category Achievement Matrix

### Key Insights

- Emily Burns achieved the highest sales and profit.
- All managers demonstrated positive growth trends.
- Technology category contributed significantly to achievement percentages.

---

## Dashboard Preview

![Manager Performance](screenshots/manager_performance.png)

---

# 3️⃣ Category & Operational Performance

## Purpose

Analyze category performance and operational efficiency.

### Categories

- Technology
- Office Supplies
- Furniture

### Visualizations

- Actual Sales vs Target
- Return Rate by Region & Category
- Return Trend by Category
- Delivery Delay by Ship Mode

### Key Insights

- Technology generated the highest revenue.
- Furniture showed the lowest achievement percentage.
- Standard Class shipments experienced higher delays.

---

## Dashboard Preview

![Category Performance](screenshots/category_performance.png)

---

# 4️⃣ Risk Assessment & Recommendations

## Purpose

Identify operational risks and areas requiring business intervention.

### Visualizations

- Manager Return Rate & Delay Rate
- Managers Below Target Table
- Categories Missing Target Table
- Risk Summary Matrix
- Manager & Category Mapping

### Risk Indicators

| KPI | Status |
|-------|---------|
| Return Rate | Moderate |
| Delay Rate | High |
| Profitability | Good |
| Target Achievement | Good |

### Major Risk

🚨 High Delivery Delay Rate (**40.76%**)

### Recommended Actions

- Improve logistics planning
- Optimize warehouse operations
- Monitor shipping performance
- Analyze root causes of returns
- Review category target allocation

---

## Dashboard Preview

![Risk Assessment](screenshots/risk_assessment.png)

---

# 📐 DAX Measures Used

## Total Sales

```DAX
Total Sales =
SUM(Orders[Sales])
```

## Total Profit

```DAX
Total Profit =
SUM(Orders[Profit])
```

## Total Orders

```DAX
Total Orders =
DISTINCTCOUNT(Orders[Order ID])
```

## Profit Margin %

```DAX
Profit Margin % =
DIVIDE([Total Profit],[Total Sales],0) * 100
```

## Return Rate %

```DAX
Return Rate % =
DIVIDE([Returned Orders],[Total Orders],0) * 100
```

## Delay Rate %

```DAX
Delay Rate % =
DIVIDE([Delayed Orders],[Total Orders],0) * 100
```

## Achievement %

```DAX
Achievement % =
DIVIDE([Total Sales],[Target Sales],0) * 100
```

---

# 📌 Key Business Findings

## Sales Performance

- Total Sales exceeded **2.9 Million**
- Strong year-over-year growth
- 2018 was the best-performing year

## Profitability

- Total Profit reached **372.83K**
- Profit Margin maintained at **12.69%**

## Regional Performance

### Central Region
Highest revenue contributor

### North Region
Moderate contribution

### South Region
Growth opportunity identified

## Category Performance

### Technology
Highest sales and achievement

### Office Supplies
Stable performance

### Furniture
Lowest achievement percentage

## Operational Performance

### Return Rate
6.37%

### Delay Rate
40.76%

Delivery delays remain the primary operational challenge.

---

# 💡 Business Recommendations

### Logistics Improvement

- Improve warehouse efficiency
- Optimize shipping routes
- Monitor carrier performance

### Return Reduction

- Analyze return reasons
- Improve product quality checks
- Enhance packaging standards

### Performance Monitoring

- Introduce monthly KPI reviews
- Set manager-level targets
- Monitor category achievement regularly

---

# 🚀 Skills Demonstrated

### Power BI
- Interactive Dashboard Design
- Drill-down Analysis
- KPI Development
- Data Storytelling

### DAX
- Calculated Measures
- Performance Metrics
- Target Achievement Calculations

### Data Analysis
- Sales Analytics
- Profitability Analysis
- Operational Analysis
- Risk Assessment

### Business Intelligence
- Executive Reporting
- Strategic Recommendations
- Performance Monitoring

---

# 📁 Repository Structure

```text
Sales-Performance-Dashboard/
│
├── sale_performance.pbix
│
├── screenshots/
│   ├── Executive Business Overview.png
│   ├── Regional Manager Performance.png
│   ├── Category & Operational Performance.png
│   ├── Risk Assessment & Recommended Actions.png
│   
│
├── README.md
│
└── SalesAnalytics_dataset.xlsx
```

---

# 🎓 Learning Outcomes

This project helped strengthen skills in:

- Power BI Dashboard Development
- Data Modeling
- DAX Calculations
- KPI Design
- Business Analytics
- Sales Performance Analysis
- Operational Risk Assessment
- Data Visualization Best Practices

---

# 👨‍💻 Author

**Ayan Samanta**

Aspiring Data Analyst

### Skills
- Power BI
- SQL
- Python
- Excel
- Data Analytics
- Business Intelligence


### 📬 Contact
📧 Email: ayansamanta875@gmail.com

💼 LinkedIn: https://www.linkedin.com/in/ayan-samanta-710813246

🧑‍💻 GitHub: https://github.com/Ayan875an


---

## ⭐ If you found this project useful, please consider giving it a star!
