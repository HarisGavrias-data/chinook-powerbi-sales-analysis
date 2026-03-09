# Chinook Power BI Sales Analysis

Interactive **Power BI dashboard** analyzing music sales using the **Chinook database**.  
The project focuses on revenue analysis, customer activity, top-performing artists, and geographic sales distribution.

---

## Dashboard Preview

![Dashboard Preview](docs/images/chinook-dashboard-preview.png)

---

## Project Overview

This project analyzes sales data from the **Chinook Database**, a sample dataset that represents a digital music store.

The dashboard was built using **Power BI** to explore business insights such as revenue trends, top artists, customer distribution, and sales by country.

The goal of this analysis is to demonstrate how business intelligence tools can transform raw transactional data into actionable insights.

---

## Key Metrics

The dashboard tracks the following KPIs:

- **Revenue:** $2.33K  
- **Total Tracks Sold:** 2240  
- **Total Customers:** 59  

---

## Dashboard Features

### Top Artists by Revenue
Displays the artists generating the highest total revenue.

### Monthly Sales Trend
Shows revenue trends over time to identify patterns and changes in sales performance.

### Revenue by Country
Visualizes geographic distribution of revenue across different markets.

### Genre Filter
Interactive filter that allows users to explore sales performance by music genre.

---
chinook-powerbi-sales-analysis
│
├── README.md
├── LICENSE
│
├── docs
│   └── images
│       └── chinook-dashboard-preview.png
│
├── data
│   └── Chinook.db
│
├── pbix
│   └── chinook-sales-dashboard.pbix
│
└── dax
    └── measures.md
---
## DAX Measures

### Revenue

```DAX
revenue =
SUMX(
    'chinook invoiceline',
    'chinook invoiceline'[UnitPrice] * 'chinook invoiceline'[Quantity]
)

