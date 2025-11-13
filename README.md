# 🍕 Pizza Sales Analysis: A Data-Driven Approach to Optimizing Operations and Revenue

## 📖 Table of Contents
1. [Introduction](#introduction)
2. [Dataset & Tools](#dataset--tools)
3. [Analysis & Key Findings](#analysis--key-findings)
4. [Interactive Dashboard](#interactive-dashboard)
5. [Business Recommendations](#business-recommendations)
6. [Future Work](#future-work)
7. [Repository Structure](#repository-structure)
8. [Conclusion](#conclusion)

---

## Introduction

In the competitive food industry, understanding customer behavior and sales patterns is critical for optimizing inventory, staffing, and marketing strategies. This case study analyzes a pizza restaurant's sales data to uncover actionable insights that can drive revenue growth and improve operational efficiency. The goal is to move from raw transactional data to strategic business decisions.

---

## Dataset & Tools

The analysis is based on a set of relational CSV files that capture the entire order lifecycle:

- **`orders.csv`**: Contains high-level order information (`Order Id`, `Date`, `Time`).
- **`order_details.csv`**: Links orders to specific pizzas and quantities.
- **`pizzas.csv`**: Details about each pizza, including its size and price.
- **`pizza_types.csv`**: Provides categorical information for each pizza type (e.g., 'Classic', 'Veggie').

**Primary Tool**: Tableau was used for data visualization and creating an interactive dashboard to explore trends and patterns. Python (Pandas) could be used for initial data cleaning and aggregation.

---

## Analysis & Key Findings

The analysis was broken down into key business questions, each addressed through a specific visualization in our dashboard.

### 3.1. What Are Our Best-Selling Pizzas?

The **"Bestsellers"** chart clearly identifies the top-performing products.
- **🥇 Top Seller**: The `big_meat_s` (Big Meat, Small) is the undisputed champion with **1,914 units sold**.
- **🥈 Runners-Up**: `thai_ckn_l` and `five_cheese_l` followed with approximately **1,410 units** each.
- **📉 Trend**: Sales volume generally decreases as we move down the list of pizza IDs.

> **Insight**: Marketing efforts and prime real estate on the menu should be dedicated to the top 5-10 bestsellers to maximize visibility and sales.

### 3.2. When Are Our Peak Ordering Hours?

The **"Peak Hours"** analysis reveals critical staffing and inventory windows.
- **🌆 Lunch Rush**: A massive spike occurs at **12:00 PM** with **6,776 pizzas ordered**.
- **🌆 Evening Rush**: A second, broader peak occurs between **4:00 PM and 5:00 PM**, with orders exceeding **5,000**.
- **🌙 Late Night**: Demand steadily declines after 7:00 PM, dropping below 2,500 orders per hour.

> **Insight**: Schedule the majority of kitchen and delivery staff for 11:30 AM - 1:30 PM and 3:30 PM - 6:00 PM to handle peak demand efficiently.

### 3.3. How Do Different Categories and Sizes Perform?

The **"Category Analysis"** and **"Size Based Analysis"** charts provide a high-level view of product performance.

| Metric | Top Category | Top Size |
| :--- | :--- | :--- |
| **Total Sales** | Classic ($220,053) | Small (S) ($178,077) |
| **Total Quantity**| Classic (14,888 units) | Small (S) (14,403 units)|

> **Insight**: While "Classic" pizzas generate the most revenue, the "Small" size is the most popular by quantity. This suggests a strategy focused on high-volume small-pizza combos and premium-priced "Classic" options.

### 3.4. What Is Our Typical Customer's Ordering Behavior?

The **"Top Customers"** and **"Pizza per order"** charts shed light on order composition.
- **📊 Order Size**: The vast majority (~70%) of customers order **1 or 2 pizzas per order**.
- **📈 Bulk Orders**: While rare, there are outliers, with one order containing **21 distinct pizzas**.
- **📉 Drop-off**: The number of orders decreases sharply as the pizza count per order increases beyond 4.

> **Insight**: Marketing promotions (e.g., "Buy One, Get One 50% Off") are well-suited for the majority of customers. Special catering or bulk-order packages could be developed to capture the high-value outliers.

---

## Interactive Dashboard

All these insights were consolidated into a single, interactive Tableau dashboard. This allows stakeholders to explore the data dynamically, filter by date or category, and drill down into specific metrics. The dashboard includes tabs for:
- Bestsellers
- Peak Hours
- Category Analysis
- Size Based Analysis
- Top Customers
- Daily/Monthly Sales Trends

---

## Business Recommendations

Based on the analysis, we propose the following data-driven actions:

1.  **Optimize Staffing & Inventory**: Align staff schedules and ingredient prep with the 12 PM and 4-5 PM peak hours to reduce wait times and waste.
2.  **Create Targeted Promotions**:
    - Launch a "Classic Pizza of the Week" feature to promote the highest-revenue category.
    - Offer combo deals centered around the popular Small size to increase average order value.
3.  **Refine Menu Strategy**: Ensure the top 5 bestsellers are prominently featured on the menu and in marketing materials. Consider discontinuing or re-promoting the lowest-selling items.
4.  **Develop a Catering Strategy**: Create a dedicated "Party & Catering" menu to capture the small but high-value bulk-order segment.

---

## Future Work

This analysis provides a solid foundation, but further opportunities exist:

- **Customer Segmentation**: Use clustering techniques to identify distinct customer groups (e.g., "Lunch Regulars," "Weekend Families," "Bulk Orderers").
- **Market Basket Analysis**: Determine which pizzas are frequently ordered together to create smarter combo deals.
- **Predictive Forecasting**: Develop a time-series model to forecast daily or hourly sales, enabling even more precise inventory and staffing management.

---

## Repository Structure

```
pizza-sales-analysis/
├── data/
│   ├── orders.csv
│   ├── order_details.csv
│   ├── pizzas.csv
│   └── pizza_types.csv
├── notebooks/
│   └── 01_data_exploration.ipynb   # (Optional) For initial data cleaning with Python/Pandas
├── visualizations/
│   └── pizza_sales_dashboard.twb   # Tableau Workbook
└── README.md                       # This file
```

---

## Conclusion

This project demonstrates how transactional data can be transformed into a strategic asset. By visualizing and analyzing sales trends, we have identified clear opportunities to enhance operational efficiency, boost marketing effectiveness, and ultimately increase revenue for the pizza business. The interactive dashboard serves as a living tool for ongoing data-driven decision-making.
