# 🍕 Pizza Sales & Performance Dashboard (Power BI)
![pizza sales dashbord](https://github.com/user-attachments/assets/6495db21-2af2-43a7-b6cf-97c2bc69c189)

## 📌 Project Overview

This project is a **professional Power BI dashboard** built to analyze pizza sales data and convert raw transactional data into **actionable business insights**. The dashboard focuses on sales performance, customer ordering behavior, and product-level analysis.

The goal of this project is to demonstrate **end-to-end data analytics skills** including data modeling, DAX calculations, and clean dashboard design.

---

## 📊 Dashboard Highlights

* Total Revenue, Total Orders & Total Pizzas Sold
* Average Order Value (AOV)
* Average Pizzas per Order
* Sales trend analysis by **Month & Day**
* Order distribution by **Time Slots** (Breakfast, Lunch, Evening, Dinner)
* Revenue & quantity analysis by **Pizza Category & Size**
* **Top 5 & Bottom 5 pizzas** by revenue
* Key Insights box for quick decision-making

---

## 🧮 Key DAX Measures Used

* **Total Revenue**
  `SUM(pizza_sales[total_price])`

* **Total Orders**
  `DISTINCTCOUNT(pizza_sales[order_id])`

* **Total Pizzas Sold**
  `SUM(pizza_sales[quantity])`

* **Average Order Value**
  `DIVIDE([Total Revenue], [Total Orders])`

* **Average Pizzas per Order**
  `DIVIDE([Total Pizzas Sold], [Total Orders])`

* **Order Hour**
  `HOUR(pizza_sales[order_time])`

* **Time Slot Column**

  ```
  Time Slot =
  SWITCH(
      TRUE(),
      HOUR(pizza_sales[order_time]) >= 6 && HOUR(pizza_sales[order_time]) < 12, "Breakfast",
      HOUR(pizza_sales[order_time]) >= 12 && HOUR(pizza_sales[order_time]) < 16, "Lunch",
      HOUR(pizza_sales[order_time]) >= 16 && HOUR(pizza_sales[order_time]) < 20, "Evening",
      "Dinner"
  )
  ```

---

## 📈 Key Insights

* Dinner time generates the **highest number of orders**
* **Large-size pizzas** contribute the maximum revenue
* Weekends show **higher demand** compared to weekdays

---

## 🛠 Tools & Technologies

* Power BI
* DAX
* Data Visualization

---

## 🎯 Learning Outcomes

* Understanding business KPIs and metrics
* Writing optimized DAX measures
* Designing clean, professional dashboards
* Converting data into insights for decision-making

---

## 📂 Dataset

The dataset contains pizza sales transaction data including:

* Order ID & Order Time
* Pizza Name, Category & Size
* Quantity Sold
* Total Price

---

## 🚀 How to Use

1. Open the `.pbix` file in Power BI Desktop
2. Explore slicers for Category & Size
3. Analyze trends and insights across visuals

---

## 📬 Feedback

Suggestions and feedback are welcome to improve this dashboard further.

---

**Author:** Amit
**Role:** Data Analyst / Freelancer
