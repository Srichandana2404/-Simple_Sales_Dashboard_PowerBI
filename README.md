# -Simple_Sales_Dashboard_PowerBI

# 📊 Power BI Task 8 – Sales Dashboard with Time-Based Analysis

## 🧭 Overview

This Power BI dashboard visualizes sales performance using the "Sample - Superstore" dataset. It includes interactive visuals such as line charts, bar charts, donut charts, and slicers to explore sales, profit, and quantity across regions and product categories. A key challenge addressed in this task was converting a text-based `Order Date` column into a usable format for time-based analysis.

---

## 🔧 Data Transformation

The original `Order Date` column was stored as **text**, which prevented proper time grouping. To enable month-year analysis, two DAX transformations were applied:

### 1️ Convert Text to Proper Date Format

DAX
CleanDate = DATEVALUE('Sample - Superstore'[Order Date])

### 2  Extract Month and Year from Converted Date
MonthYear = FORMAT([CleanDate], "MMM YYYY")


This formula formats the cleaned date into a readable Month-Year string (e.g., "Jul 2016"), ideal for use in visuals and slicers.

📈 Visuals Included
- Line Chart: Sales over time (MonthYear on X-axis, Sales on Y-axis)
- Bar Chart: Sales by region (Region on X-axis, Sales on Y-axis)
- Donut Chart: Sales by category (Category as legend, Sales as values)
- Slicer: Interactive filtering by Region or Category

