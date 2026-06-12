# 📊 Sales Performance Dashboard | Business Review (2015–2018)

<img width="983" height="555" alt="Screenshot 2026-06-12 203354 - Copy" src="https://github.com/user-attachments/assets/21c72ef3-01ae-4bc5-8906-3784c46612b3" />


---

# 📌 Project Overview

This Power BI dashboard provides a comprehensive business performance review from **2015 to 2018**. The project focuses on analyzing sales, profit, orders, targets, return rates, delivery delays, regional performance, manager effectiveness, and category achievements.

The dashboard is designed to help decision-makers monitor business health, identify operational risks, evaluate target achievement, and uncover opportunities for growth.

---

# 🎯 Business Problem

Management needed a centralized dashboard to answer the following questions:

- How is the company performing overall?
- Which regions generate the highest sales?
- Which Regional Managers perform best?
- Are sales targets being achieved?
- Which product categories contribute the most revenue?
- How have sales and profits changed over time?
- What is the impact of returns and delayed deliveries?
- Which business areas require immediate attention?

---

# 📂 Dataset Information

The dashboard is built using business sales data containing:

### Orders Data
- Order ID
- Order Date
- Sales
- Profit
- Region
- Category
- Ship Mode
- Regional Manager

### Returns Data
- Returned Orders

### Target Data
- Category Targets
- Performance Benchmarks

---

# 🛠️ Tools & Technologies

| Tool | Purpose |
|--------|----------|
| Power BI Desktop | Dashboard Development |
| Power Query | Data Cleaning & Transformation |
| DAX | Calculated Measures |
| Excel | Data Source |
| Data Modeling | Relationships & Analytics |

---

# 📈 Dashboard Structure

The report consists of **4 interactive pages**.

---

# Page 1: Executive Business Overview

## Objective
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
- Year-over-Year Comparison Table
- Year Filter Slicer

### Key Insights

- Sales increased consistently between 2015 and 2018.
- 2018 recorded the highest revenue and profit.
- Central region contributed the largest share of total sales.
- Profit growth followed sales growth throughout the period.

---

# Page 2: Regional Manager Performance

## Objective
Analyze Regional Manager contributions and performance.

### Managers Covered

- Emily Burns
- Ross DeVincentis
- Damala Kotsonis

### Visualizations

- Manager KPI Cards
- Manager Ranking Chart
- Year-over-Year Sales Trend
- Manager × Category Achievement Matrix

### Key Insights

#### Emily Burns
- Highest Sales Contribution
- Highest Profit Contribution

#### Ross DeVincentis
- Strong Profitability
- Moderate Sales Performance

#### Damala Kotsonis
- Consistent Performance Across Categories

### Business Value

Helps leadership identify:
- Top-performing managers
- Growth opportunities
- Performance gaps

---

# Page 3: Category & Operational Performance

## Objective
Evaluate category performance against targets and operational efficiency.

### Categories Analyzed

- Technology
- Office Supplies
- Furniture

### Visualizations

#### Sales vs Target by Category
Compare actual sales with category targets.

#### Return Rate by Region & Category
Identify categories with high return percentages.

#### Return Rate Trend Analysis
Track return rates across years.

#### Delivery Delay Analysis
Analyze delays by ship mode.

### Key Insights

### Technology
- Highest Sales
- Highest Target Achievement

### Office Supplies
- Strong and Stable Performance

### Furniture
- Lowest Achievement Percentage

### Shipping Analysis

#### Standard Class
- Highest delay percentage

#### Second Class
- Lower delay percentage

---

# Page 4: Risk Assessment & Recommendations

## Objective
Identify operational risks and provide actionable recommendations.

### Visualizations

- Manager Return Rate & Delay Rate
- Managers Below Target Table
- Categories Missing Target Table
- Risk Summary Matrix
- Regional Manager & Category Mapping

---

# Risk Assessment Framework

| KPI | Risk Level |
|-------|-------------|
| Return Rate | Medium |
| Delay Rate | High |
| Target Achievement | Low Risk |
| Profitability | Low Risk |

---

# Major Risk Identified

## High Delivery Delays

Average Delay Rate:

**40.76%**

### Potential Impact

- Customer dissatisfaction
- Increased returns
- Reduced customer retention
- Lower operational efficiency

---

# Recommended Actions

### Logistics Optimization

- Improve warehouse processes
- Optimize inventory placement
- Reduce shipping bottlenecks

### Delivery Performance Monitoring

- Track carrier performance
- Establish delivery SLAs
- Monitor delays monthly

### Return Reduction Strategy

- Analyze return reasons
- Improve product quality
- Improve packaging standards

### Target Management

- Introduce manager-specific targets
- Review category targets quarterly

---

# 📊 DAX Measures Used

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
DIVIDE([Total Profit],[Total Sales],0)*100
```

## Return Rate %

```DAX
Return Rate % =
DIVIDE([Returned Orders],[Total Orders],0)*100
```

## Delay Rate %

```DAX
Delay Rate % =
DIVIDE([Delayed Orders],[Total Orders],0)*100
```

## Achievement %

```DAX
Achievement % =
DIVIDE([Total Sales],[Target Sales],0)*100
```

---

# 📌 Key Business Findings

## Revenue Growth

- Total Sales exceeded **2.9 Million**
- Continuous growth observed every year

## Profitability

- Total Profit exceeded **372K**
- Profit Margin maintained at **12.69%**

## Regional Performance

### Central Region
- Highest revenue contributor

### North Region
- Moderate contribution

### South Region
- Growth opportunity identified

## Category Performance

### Technology
- Best-performing category

### Furniture
- Lowest target achievement

## Operations

### Return Rate
- 6.37%

### Delay Rate
- 40.76%

Delivery delays represent the most significant operational challenge.

---

# 🚀 Skills Demonstrated

### Power BI

- Interactive Dashboard Design
- Drill-down Analysis
- KPI Development
- Data Storytelling

### DAX

- Calculated Measures
- KPI Calculations
- Percentage Metrics
- Target Achievement Analysis

### Data Analysis

- Sales Analysis
- Profitability Analysis
- Risk Assessment
- Performance Tracking

### Business Intelligence

- Executive Reporting
- Performance Monitoring
- Operational Insights
- Strategic Recommendations

---

# 📷 Dashboard Screenshots

## Executive Overview

![Executive Overview](screenshots/executive_overview.png)

## Regional Manager Performance

![Manager Performance](screenshots/manager_performance.png)

## Category Performance

![Category Performance](screenshots/category_performance.png)

## Risk Assessment

![Risk Assessment](screenshots/risk_assessment.png)

---

# 📁 Repository Structure

```text
Sales-Performance-Dashboard/
│
├── Sales_Performance_Dashboard.pbix
│
├── screenshots/
│   ├── executive_overview.png
│   ├── manager_performance.png
│   ├── category_performance.png
│   └── risk_assessment.png
│
├── dataset/
│   ├── Orders.xlsx
│   ├── Returns.xlsx
│   └── Targets.xlsx
│
└── README.md
```

---

# 🎓 Learning Outcomes

Through this project, I strengthened my skills in:

- Power BI Dashboard Development
- Data Modeling
- DAX Calculations
- Business KPI Design
- Sales Analytics
- Performance Monitoring
- Risk Assessment
- Data Visualization Best Practices

---

# 👨‍💻 Author

## Ayan

Aspiring Data Analyst

### Skills
- Power BI
- SQL
- Python
- Excel
- Data Visualization
- Business Intelligence

---

# ⭐ If you found this project useful, please give it a star!
