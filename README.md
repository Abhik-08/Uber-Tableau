# 🚗 Uber Ride Analytics Dashboard — Tableau | 2024

<p align="center">
  <img src="Uber logo.png" alt="Uber Logo" width="120"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Tool-Tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white"/>
  <img src="https://img.shields.io/badge/Data-Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white"/>
  <img src="https://img.shields.io/badge/Domain-Ride%20Analytics-black?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Year-2024-1A1A1A?style=for-the-badge"/>
</p>

---

## 📌 Project Overview

An interactive **Tableau dashboard** built on top of a comprehensive Uber ride-sharing dataset sourced from Kaggle, covering **148,770 total bookings** across the full year of 2024. The dashboard surfaces key insights around booking trends, revenue patterns, trip distance distribution, pickup hotspots, and hourly demand — all in a clean, dark-themed analytical layout.

> 💡 **Goal:** Transform raw ride-sharing data into actionable, visual business intelligence using Tableau's full suite of chart types and KPI cards.

---

## 📊 Dashboard Preview

![Uber Analytics Dashboard](1774687064092_image.png)

---

## 🔢 Key KPIs at a Glance

| Metric | Value |
|---|---|
| 📦 Total Bookings | **148.77K** |
| 💰 Total Booking Value | **₹51.85M** |
| 📍 Avg. Booking Value | **₹508.3** |
| 📏 Avg. Ride Distance | **24.64 km** |
| ✅ Success Rate | **65.96%** (~93K rides) |
| ❌ Cancellation Rate | **25%** (~37.43K rides) |
| 🙋 Customer Cancellations | **19.15%** (~27K rides) |
| 🚘 Driver Cancellations | **7.45%** (~10.5K rides) |

---

## 📁 Dataset Details

- **Source:** [[Kaggle — Uber Ride Analytics Dataset 2024](https://www.kaggle.com/](https://www.kaggle.com/datasets/yashdevladdha/uber-ride-analytics-dashboard))
- **Records:** 148,770 bookings
- **Temporal Coverage:** 01 Jan 2024 → 30 Dec 2024 (full year, daily granularity)
- **Geographic Scope:** Multiple pickup & drop locations (Delhi NCR area)

### 📋 Schema

| Column | Description |
|---|---|
| `Date` / `Time` | Booking timestamp |
| `Booking ID` | Unique ride identifier |
| `Booking Status` | Completed / Cancelled by Customer / Cancelled by Driver |
| `Customer ID` | Unique customer identifier |
| `Vehicle Type` | Go Mini, Go Sedan, Auto, eBike/Bike, UberXL, Premier Sedan |
| `Pickup Location` | Starting point of the ride |
| `Drop Location` | Ride destination |
| `Avg VTAT` | Avg. driver arrival time at pickup (mins) |
| `Avg CTAT` | Avg. trip duration from pickup to destination (mins) |
| `Booking Value` | Fare amount (₹) |
| `Ride Distance` | Distance covered (km) |
| `Driver Ratings` | Rating given to driver (1–5) |
| `Customer Rating` | Rating given by customer (1–5) |
| `Payment Method` | UPI / Cash / Credit Card / Uber Wallet / Debit Card |
| `Cancellation Reasons` | Reasons captured for both customer & driver cancellations |

---

## 📈 Worksheets & Visualizations

The dashboard contains the following **9 worksheets** compiled into a single interactive dashboard:

| # | Worksheet | Chart Type | Insight |
|---|---|---|---|
| 1 | **Total Trips by Month** | Area / Line Chart | Monthly booking volume trend over 2024 |
| 2 | **Revenue by Month** | Area Chart | Monthly revenue fluctuation |
| 3 | **Revenue by Pickup Location – Top 10** | Horizontal Bar Chart | Highest revenue-generating pickup zones |
| 4 | **Total Bookings by Day** | Bar Chart | Day-of-week booking distribution |
| 5 | **Total Bookings by Hour** | Bar Chart | Hourly demand pattern (peak hours) |
| 6 | **Trip Distance Distribution** | Histogram | Frequency distribution of ride distances |
| 7 | **Fare vs. Distance** | Scatter Plot | Correlation between fare amount and ride distance |
| 8 | **Average Fare by Distance Bucket** | Bar Chart | Fare breakdown across 4 distance bands |
| 9 | **KPI Cards** | KPI Tiles | Total Bookings, Total Value, Avg Booking Value, Avg Distance |

---

## 🔍 Key Insights

### 📅 Temporal Trends
- Booking volumes remain **relatively stable month-over-month**, ranging between ~12,000–13,500 trips/month with mild dips mid-year.
- **Peak hours** are clearly skewed toward the **evening (17:00–22:00)**, reflecting post-work commute demand.
- Day-of-week distribution is nearly **uniform (~21,000–21,600 bookings/day)** with no single day dominating significantly.

### 📍 Location Insights
- **Barakhamba Road** leads all pickup locations with **₹341.15K** in total revenue, followed closely by **Khandsa (₹338.5K)** and **Subhash Chowk (₹329.39K)**.
- The top 10 pickup locations are tightly clustered in revenue (₹322K–₹341K), indicating **broad geographic demand**.

### 💸 Revenue & Fare Insights
- The **Fare vs. Distance scatter plot** shows a dense cluster between ₹500–₹2,500 for most short-to-medium rides, with thin high-value outliers for long-distance bookings.
- Interestingly, **average fare across distance buckets** stays remarkably consistent: ₹513 (0–3 km), ₹500 (3–7 km), ₹504 (7–15 km), ₹510 (15+ km) — suggesting **flat-ish fare structure** with surge pricing being a key differentiator.

### 🚗 Fleet Performance
| Vehicle Type | Avg. Distance | Success Rate |
|---|---|---|
| Auto | 25.99 km | 91.1% |
| eBike/Bike | 26.11 km | 91.1% |
| Go Mini | 25.99 km | 91.0% |
| Go Sedan | 25.98 km | 91.1% |
| Premier Sedan | 25.95 km | 91.2% |
| UberXL | 25.72 km | 92.2% |

### 🚫 Cancellation Patterns
**Customer Cancellations (19.15%):**
- Wrong Address: 22.5%
- Driver Issues: 22.4%
- Driver Not Moving: 22.2%
- Change of Plans: 21.9%
- App Issues: 11.0%

**Driver Cancellations (7.45%):**
- Customer-Related Issues: 25.3%
- Capacity Issues: 25.0%
- Personal & Car Issues: 24.9%
- Customer Behavior: 24.8%

### ⭐ Ratings
- **Customer Ratings** are consistently high across all vehicle types: **4.40–4.41**
- **Driver Ratings** are slightly lower but stable: **4.23–4.24**
- Highest rated vehicle: **Go Sedan** (4.41 customer rating)

### 💳 Payment Method Share
| Method | Revenue Share |
|---|---|
| UPI | ~40% |
| Cash | ~25% |
| Credit Card | ~15% |
| Uber Wallet | ~12% |
| Debit Card | ~8% |

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Tableau Desktop / Public** | Dashboard creation & visualization |
| **Microsoft Excel / CSV** | Data source (Uber.csv) |
| **Kaggle** | Dataset origin |

---

## 🚀 How to Use

1. **Clone this repository**
   ```bash
   git clone https://github.com/Abhik-08/uber-tableau-dashboard.git
   cd uber-tableau-dashboard
   ```

2. **Open the Tableau workbook**
   - Open `Uber_Dashboard.twbx` in **Tableau Desktop** or **Tableau Public**

3. **Explore the Dashboard**
   - Use the **Date slider** to filter bookings by time range
   - Use the **Pickup Location dropdown** to filter by specific zones
   - Navigate between worksheets using the tabs at the bottom

4. **Dataset**
   - Raw data: `Uber.csv`
   - Can be re-connected via `Data > Edit Data Source` in Tableau

---

## 🌐 Live Dashboard

> 🔗 View the published dashboard on Tableau Public:  
> **[🚗 Uber Ride Analytics Dashboard 2024 → Click to View](https://public.tableau.com/views/UberDashboard_17745510068850/Dashboard1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)**

---

## 🙋‍♂️ Author

**Abhik** — CSE Student, Dr. B.C. Roy Engineering College, Durgapur  
📎 [LinkedIn](https://www.linkedin.com/in/abhik-mukherjee-b6a15920a/) | 🐙 [GitHub](https://github.com/Abhik-08)

---

## 📜 License

This project is open-source under the [MIT License](LICENSE).  
Dataset sourced from Kaggle and used for educational & portfolio purposes only.

---

<p align="center">
  Made with ❤️ and Tableau | <b>Uber Ride Analytics 2024</b>
</p>
