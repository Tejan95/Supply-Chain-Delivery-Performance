# Supply Chain Delivery Performance Analysis

## 📌 Project Overview
This project targets global supply chain logisitical bottlenecks by evaluating **180,519 historical orders** across **6 global markets**. Utilizing **Power BI**, this interactive dashboard tracks delivery delays, maps shipping modes against real-world scheduling gaps, and isolates high-revenue priority zones to optimize international distribution strategies.

---

## 📊 Key Business Outcomes & Insights

### 🚚 1. Delivery Efficiency & Shipping Mode Mismatches
* **The Insight:** The global logistical network is experiencing a systemic **54.8% late delivery rate**. 
* **The Root Cause:** Delays are primarily driven by **Standard Class shipments**, which account for **59.7% of all total order volumes**, severely throttling transit processing capacities.

### ⏱️ 2. Fulfillment Scheduling Gaps
* **The Insight:** Analysis uncovered an average **0.6-day operational gap** between scheduled shipping dates and actual dispatch times.
* **Regional Bottlenecks:** Central America and Western Europe recorded the highest concentration of total order volumes, amplifying the systemic delivery delays due to regional fulfillment center strain.

### 💰 3. Regional Revenue Impact & Market Prioritization
* **The Insight:** Streamlining shipping selections can directly protect high-value markets. 
* **Priority Targets:** **Europe** and **LATAM** (Latin America) were identified as the highest-grossing priority territories, generating **$10.8M** and **$10.3M** in total revenue respectively.

---

## 🖥️ Dashboard UI Preview

### Executive Logistical Summary
![Executive Summary](./dashboard_snapshots/Screenshot%202026-06-10%20174506.png)

### Regional Shipping Deep-Dive
![Shipping Performance](./dashboard_snapshots/Screenshot%202026-06-10%20174601.png)

---

## 🛠️ Tech Stack & DAX Expressions Used
* **BI Tool:** Power BI Desktop 
* **Data Engineering:** Power Query (ETL pipeline, column profiling, data type casting, and schema normalization).
* **Key Core Metrics Designed (DAX):**
  ```dax
  Late Delivery Rate = 
  DIVIDE(
      CALCULATE(COUNT(Orders[OrderID]), Orders[DeliveryStatus] = "Late"), 
      COUNT(Orders[OrderID]), 
      0
  )

  📁 Supply-Chain-Performance (Repository Root)
 ├── 📁 dashboard_snapshots
 │    ├── Screenshot 2026-06-10 174506.png   # Primary executive dashboard snapshot
 │    └── Screenshot 2026-06-10 174601.png   # Shipping performance deep-dive view
 ├── Supply_Chain_Delivery_Analysis.pbix     # Master Power BI application file
 └── README.md                               # Analytical executive presentation
