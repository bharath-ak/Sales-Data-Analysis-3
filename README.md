# 📊 Amazon Products | Sales Analysis Dashboard

This repository contains a Power BI dashboard designed to analyze and visualize **Amazon product sales** across various product categories. It provides insights into **Year-To-Date (YTD) Sales**, **Quantity**, **Reviews**, and trends by **month**, **week**, and **product performance**.

## 🔗 Live Dashboard

👉 [View Power BI Report](https://app.powerbi.com/view?r=eyJrIjoiYjkyOTkxMDItZTljZC00ZGExLWIzNDctMTMxZTBjNzMwNjVmIiwidCI6ImM2MDlhZTI5LTBkMjQtNDU4My04NzRjLTFkYTVhMTg5OTk1ZSJ9)

---

## 🧩 Features

- 📅 **Time-Based Analysis**: Sales by Month and Week.
- 📦 **Category Filters**: Dynamic filtering by Product Category and Quarter.
- 🔍 **KPIs**:
  - YTD Sales
  - QTD Sales
  - YTD Quantity
  - YTD Reviews
- 📈 **Top Performing Products**:
  - Top 5 by Sales
  - Top 5 by Reviews
- 📋 **Detailed Table View** by Product Category.

---

## 📌 DAX Snippets

-- Extract Month from Date
Month = FORMAT('Table'[Date], "MMM")

-- YTD Sales Measure
YTD Sales = TOTALYTD(SUM('Sales'[Amount]), 'Sales'[Date])

-- QTD Sales Measure
QTD Sales = TOTALQTD(SUM('Sales'[Amount]), 'Sales'[Date])

-- YTD Quantity Measure
YTD Quantity = TOTALYTD(COUNT(Amazon_Data[Product Category]),'Date Table'[Date])

-- YTD Reviews Measure
YTD Reviews = TOTALYTD(SUM(Amazon_Data[Number of  reviews]),'Date Table'[Date])

---

## 🔍 Insights

- Sales seasonality and trends
- Best-selling products
- Customer review patterns
- Quarter-wise performance breakdown
