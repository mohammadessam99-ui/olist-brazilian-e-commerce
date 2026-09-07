# 📊 Olist E-Commerce Business Intelligence & Power BI Dashboard

## 📌 Project Overview
An end-to-end Power BI Business Intelligence solution built on the **Olist Brazilian E-Commerce Dataset**. This interactive multi-page dashboard translates complex transactional and logistics data into actionable insights—evaluating sales trends, seller performance, geographic distribution, fulfillment timelines, and customer satisfaction.

---
Data Architecture & Star Schema Model

The data model follows a **Star Schema** architecture (with normalized snowflake lookup entities) designed for high query efficiency, complex DAX time intelligence, and granular cross-functional analytics across orders, fulfillment, products, and customer feedback.

![Data Model Architecture](Analysis%20Project/DataModel.png)

### 1. Fact Tables
* **`Order Items Dataset`**: Core transactional fact table capturing item-level revenue metrics (`price`, `freight_value`) linked to products, sellers, and order headers.
* **`Order Dataset`**: Order-level fact table storing operational status timestamps (`purchase`, `approved`, `carrier_delivered`, `customer_delivered`, `estimated_delivery`) used for supply chain lead-time analytics.
* **`Target`**: Fact table storing target goal benchmarks linked directly to the date dimension for KPI achievement tracking.

### 2. Dimension Tables
* **`Dim_Date`**: Dedicated calendar dimension supporting advanced DAX Time Intelligence calculations (YoY, MoM growth comparisons).
* **`Customer Dataset`**: Stores customer identifiers (`Customer Id`, `Customer Unique Id`) and regional location attributes.
* **`Seller Dataset`**: Stores vendor identifiers and seller region details for vendor performance tracking.
* **`Product Dataset` & `Product Category Name`**: Catalog dimension hierarchies classifying item categories for revenue and profitability analysis.
* **`Order Payment` & `Order Review`**: Dimension and detail tables tracking payment types, installment plans, sentiment feedback, and review scores.

---
## 🖥️ Dashboard Breakdown & Visuals

### 1. Executive Performance & Sales Overview
Provides a high-level summary of core business KPIs, target achievements, payment preferences, and Month-over-Month (MoM) performance.
* **Key Metrics:**
  * **Total Sales:** $7.34M (+68.28% Sales vs Last Year)
  * **Total Profit:** $6.08M (+66.03% Profit vs Last Year)
  * **Total Orders:** 54,011 (+69.40% Orders vs Last Year)
  * **Total Cost Freight:** $1.26M
  * **Target Achievement:** 89% Sales Achievement Rate | 89% Profit Achievement Rate
* **Payment Preference:** Credit Card dominates total payment volume (**78.81%**), followed by Boleto (**16.82%**).

![Executive Performance Overview](https://raw.githubusercontent.com/mohammadessam99-ui/olist-brazilian-e-commerce/main/OverView.png)

![Executive Performance Comparison](https://raw.githubusercontent.com/mohammadessam99-ui/olist-brazilian-e-commerce/main/OverView%20Comparing.png)

---

### 2. Year-over-Year (YoY) & Sales Performance Analysis
Tracks multi-year historical revenue trends, monthly growth fluctuations, and product category profitability using dynamic metric switches.
* **Monthly Revenue & Growth:** Features interactive toggle buttons (*Total Sales*, *Total Profit*, *Total Cost Freight*) to track MoM growth percentage variations (e.g., peak growth periods exceeding **+103.97%** MoM).
* **Profitability Matrix:** Includes a scatter plot analyzing the correlation between Total Sales and Total Profit by month, alongside top profit-generating categories led by *Watches & Gifts* and *Health & Beauty*.

![Sales & YoY Analysis](https://raw.githubusercontent.com/mohammadessam99-ui/olist-brazilian-e-commerce/main/Sales.png)

---

### 3. Seller Performance & Geographic Analysis
Combines geospatial mapping with granular seller analytics to evaluate vendor efficiency, processing delays, and regional fulfillment performance.
* **Geospatial Mapping:** Interactive map visualizing seller and order density across regions.
* **Seller Operations Metrics:** Analyzes **36,368 orders** across vendors with an average seller processing time of **6.28 days** and an overall seller return rate of **1.23%**.
* **Fulfillment Efficiency:** Tracks delivery lead times (**10.79 days actual** vs. **26.26 days estimated**), highlighting a **15.47-day shipping gap** (delivering ahead of estimated dates).

![Seller Performance](https://raw.githubusercontent.com/mohammadessam99-ui/olist-brazilian-e-commerce/main/Seller.png)

---

### 4. Product & Category Deep-Dive
Analyzes order distribution, revenue drivers, and profit margins across key product lines.

![Product Analysis](https://raw.githubusercontent.com/mohammadessam99-ui/olist-brazilian-e-commerce/main/Product.png)

---

### 5. Customer & Geographic Demographics
Examines customer geographic distribution across Brazilian states (e.g., SP, RJ, MG), purchasing frequency, average order value, and payment installment behavior.

![Customer Demographics](https://raw.githubusercontent.com/mohammadessam99-ui/olist-brazilian-e-commerce/main/Customers.png)

---

### 6. Supply Chain & Logistics Management
Monitors fulfillment efficiency, delivery lead times, shipping gaps, and return rates across price ranges and product categories.

![Logistics & Returns](https://raw.githubusercontent.com/mohammadessam99-ui/olist-brazilian-e-commerce/main/Return.png)

---

### 7. Customer Reviews & Service Quality
Tracks review scores (4.09 average score), sentiment distribution, and the direct correlation between on-time vs. late deliveries and overall customer rating.

![Customer Reviews](https://raw.githubusercontent.com/mohammadessam99-ui/olist-brazilian-e-commerce/main/Ratting.png)

---

## 🛠️ Tools & Technical Implementation
* **Power BI & DAX:** Advanced Time Intelligence DAX measures for YoY/MoM comparisons (`Sales vs Last Year`, `Sales MoM Growth %`), dynamic metric switches, and custom visuals.
* **Data Modeling:** Designed a Star Schema establishing relationships across Orders, Customers, Products, Sellers, Payments, and Geolocation datasets.
* **Power Query ETL:** Data cleaning, date table generation, column normalizations, and key transformation steps.

---

## 🎯 Key Business Insights
1. **Strong Year-over-Year Expansion:** Annual sales grew by **+68.28%** and order volume increased by **+69.40%**, showing rapid platform scaling.
2. **Delivery Speed Over-Performance:** Actual fulfillment averages **10.79 days**, significantly outperforming the **26.26-day estimated lead time**, driving positive customer satisfaction.
3. **Seller Processing Bottlenecks:** Vendor processing averages **6.28 days**, representing a key operational area for supply chain optimization.
