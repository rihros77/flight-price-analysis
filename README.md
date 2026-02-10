# ✈️ Flight Price Analytics & Revenue Optimization Dashboard

## 📌 Project Overview

This project analyzes flight pricing data to uncover **key drivers of ticket prices** and identify **revenue optimization opportunities** for airlines.

The project follows a complete **end-to-end data analytics pipeline**:
SQL → Python → Feature Engineering → Power BI Dashboard.

The final output is an executive-ready Power BI dashboard designed for airline revenue and pricing teams.

---

## 🎯 Business Problem

Airlines constantly adjust ticket prices based on demand, duration, routes, and competition.

This project answers key business questions:

* What factors influence ticket prices?
* Which routes generate premium revenue?
* Which routes are underpriced and need optimization?
* When should airlines adjust pricing strategies?

---

## 🧰 Tech Stack

* **SQL (PostgreSQL)** → Data storage & querying
* **Python (Pandas, Matplotlib, Seaborn)** → Data cleaning & feature engineering
* **Power BI** → Dashboard & visualization
* **GitHub** → Version control & portfolio

---

## 📂 Dataset Features

The dataset contains **10,000+ flight records** with:

* Airline
* Source & Destination
* Number of Stops
* Departure & Arrival Time
* Flight Duration
* Ticket Price
* Month & Day Type (Weekday/Weekend)

---

## 🧪 Data Processing & Feature Engineering (Python)

Before building the dashboard, the dataset was processed using **Python, Pandas, and PostgreSQL** to create an analytics-ready dataset.

### 1️⃣ Data Extraction

* Connected Python to PostgreSQL using `psycopg2`
* Pulled analytics table into Pandas DataFrame

### 2️⃣ Data Cleaning

* Removed **222 duplicate records**
* Verified **no missing values**
* Converted categorical columns to optimized data types

### 3️⃣ Exploratory Data Analysis (EDA)

Visual analysis performed using Matplotlib & Seaborn:

* Flight price distribution
* Price vs Airline
* Price vs Stops
* Price vs Duration
* Price vs Departure Hour
* Price vs Month

### 4️⃣ Feature Engineering

Created business-focused metrics:

| Feature                   | Description                                  |
| ------------------------- | -------------------------------------------- |
| **duration_minutes**      | Total flight duration in minutes             |
| **price_per_hour**        | Ticket price per hour of travel              |
| **rev_opportunity_score** | Revenue efficiency metric (price ÷ duration) |
| **route_segment**         | Pricing strategy classification              |

### Route Segmentation Logic

Routes were categorized to help pricing strategy:

* **Premium Route** → High price + Short duration
* **Discount Route** → Low price + Long duration
* **Optimization Route** → Remaining routes

### 5️⃣ Export for BI

Final dataset exported for Power BI:

```
flight_pricing_for_powerbi.csv
```

---

## 📊 Power BI Dashboard

The dashboard is designed for **executives and revenue managers** and contains 4 pages.

---

### 🟦 Page 1 — Executive Overview

High-level KPIs and pricing drivers.

**KPIs**

* Average Ticket Price
* Average Flight Duration
* Cheapest Airline
* Most Expensive Route

**Charts**

* Price by Airline
* Price by Month
* Price by Stops

---

### 🟩 Page 2 — Route Profitability

Shows which routes are premium vs discount vs optimization.

**Matrix Heatmap**

* Rows → Route
* Columns → Route Segment
* Values → Avg Revenue Opportunity Score

**Interactive Filters**

* Airline
* Month
* Number of Stops

---

### 🟧 Page 3 — Pricing Strategy Insights

Identifies pricing patterns and trends.

* Stops vs Price (Scatter)
* Duration vs Price (Scatter)
* Revenue Opportunity by Departure Hour

---

### 🟪 Page 4 — Revenue Management Segments

Strategic summary for pricing teams.

* Distribution of Flights by Segment
* Top Revenue Opportunities Table

---

## 🔍 Key Insights

### 💰 Pricing Drivers

* Non-stop flights have the **highest revenue efficiency**
* Longer flights are **not always more expensive**
* Departure time significantly impacts pricing

### ✨ Revenue Opportunities

* Premium routes identified for price optimization
* Discount routes reveal underpricing opportunities
* Departure hours highlight demand-based pricing windows

---

## 📁 Repository Structure

```
Flight-Price-Analytics/
│
├── Airline_Revenue_Dashboard.pbix
├── flight_pricing_for_powerbi.csv
├── flight_analysis.py
└── README.md
```

---

## 🚀 How to Run the Project

### Python Analysis

Install dependencies:

```
pip install pandas matplotlib seaborn psycopg2-binary
```

Run:

```
python flight_analysis.py
```

### Power BI Dashboard

1. Open the `.pbix` file
2. Refresh data if needed
3. Explore interactive visuals

---

## 🎓 What I Learned

* End-to-end analytics workflow
* Data cleaning & feature engineering
* Revenue strategy analytics
* Power BI dashboard design
* GitHub project publishing

---

## ⭐ Author

**Rihana Roshan**

If you liked this project, feel free to ⭐ the repo!
