# 📊 Student Analytics Dashboard

![Power BI](https://img.shields.io/badge/Data_Visualization-Power_BI-yellow?style=for-the-badge&logo=powerbi)
![DAX](https://img.shields.io/badge/Logic-DAX-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

An end-to-end Student Performance and Financial Analytics solution developed for coaching institutes. This dashboard provides actionable insights into academic trends, attendance risks, and revenue collection.

[View Demo Video](#) | [Download .pbix File](#)

---

## 📸 Dashboard Preview

<p align="center">
  <img src="https://path-to-your-main-screenshot.png" width="900" alt="Dashboard Overview">
</p>

> **Note:** This dashboard features a custom " Dark" theme, optimized for high-density data viewing and modern UI aesthetics.

---

## 🚀 Key Features

### 1. Multi-Branch KPI Tracking
* **Real-time Metrics:** High-level cards for Total Students, Avg Test Scores, and Revenue.
* **Branch Segmentation:** Compare performance across 3 distinct branches (Pune Central, Baner, Aundh).

### 2. Academic Performance & Risk Analysis
* **Attendance Alerts:** Automatically flags students with <75% attendance.
* **Performance Bands:** Categorizes students into Excellent, Good, Average, and Below Average based on test trends.
* **Correlation Mapping:** Statistical analysis of Attendance vs. Test Scores.

### 3. Financial Analytics
* **Collection Rate:** Gauge visual tracking revenue collected vs. total course fees.
* **Pending Dues:** Categorized by batch and course for targeted follow-ups.

---

## 🛠️ Tech Stack & DAX Logic

* **Tool:** Power BI Desktop
* **Data Source:** CSV / SQL (Student Management System)
* **Theme:** Custom JSON Dark Theme

### Sample Advanced DAX
```dax
-- Calculating Student Retention Risk
High Risk Count = 
COUNTROWS(
    FILTER('StudentData', 
        UPPER('StudentData'[Retention Risk]) = "HIGH"
    )
)
