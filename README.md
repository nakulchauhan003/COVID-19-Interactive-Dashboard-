# 📊 COVID-19 Interactive Dashboard

## 1. Project Title 
**COVID-19 Global Statistics Dashboard**  
A dynamic and interactive data visualization tool that helps users explore the impact of COVID-19 across different countries and continents using updated metrics from Worldometer.

---

## 2. Short Description / Purpose
The **COVID-19 Global Statistics Dashboard** is a Power BI report that visually tracks pandemic metrics including total cases, deaths, recoveries, active cases, and percentages like recovery and death rates.  
It provides an insightful overview of the pandemic’s status by region and helps users understand data trends through charts, tables, and slicers.

---

## 3. Tech Stack
This dashboard was built using the following tools and technologies:

- **Power BI Desktop** – Primary platform for visualization and dashboard creation  
- **Power Query Editor** – Used for data transformation, custom columns, and cleaning  
- **DAX (Data Analysis Expressions)** – For creating calculated measures like death rate %, recovery rate %, and active cases  
- **Data Modeling** – Relationships between countries, continents, and date filters  
- **File Formats** – `.pbix` for Power BI and `.png` for snapshots

---

## 4. Data Source

**Source:** Worldometer COVID-19 public data (manually imported or web scraped)

**Dataset Includes:**
- Country and continent names  
- Total Cases, Total Deaths, Total Recovered  
- Computed metrics like Death Rate %, Recovery Rate %, Active Cases  
- Optional: Add artificial waves (Wave 1, Wave 2) or cumulative days for timeline views

---

## 5. Features / Highlights

### • Business Problem
Lack of an easy-to-understand, dynamic visualization to track COVID-19 trends globally and regionally.

### • Goal of the Dashboard
To create an easy-to-navigate dashboard that:
- Highlights global pandemic impact with KPIs  
- Tracks trends and changes in active cases and deaths  
- Compares country-wise performance  
- Supports decision-making for healthcare planners, analysts, and researchers

---

## 6. Walkthrough of Key Visuals

- **KPI Cards:**  
  Display Total Cases, Total Deaths, Total Recovered, Active Cases, Recovery Rate %, and Death Rate % at a glance.

- **Bar Chart – Active Cases by Country:**  
  Compares the number of unresolved (active) cases per country.

- **Stacked Bar Chart – Total Deaths, Recovered, and Active Cases:**  
  Shows the overall breakdown of pandemic outcomes per country or continent.

- **Line Chart – Trend Over Time (Optional):**  
  Visualize how cases, deaths, or recoveries change over days/weeks. Use waves or relative date columns as X-axis.

- **Matrix Table – Country-wise Comparison:**  
  Includes detailed numbers per country, with columns for each major metric.

- **Decomposition Tree – Total Cases → Continent → Country:**  
  Drill-down analysis to identify where the most cases are coming from.

- **Gauge Chart – Recovered vs Total Cases:**  
  Shows progress toward full recovery (optional, use sparingly due to space).

- **Slicers – Filters:**  
  Filter by Continent, Country, and custom date/wave ranges to interactively explore data.

---

## 7. Calculated Columns / Measures Used

- **Active Cases:**  
  ```powerquery
  = [TotalCases] - [TotalDeaths] - [TotalRecovered]

- **Death Rate %:**  
  ```powerquery
  = ([TotalDeaths] / [TotalCases]) * 100

- **Recovery Rate %:**  
  ```powerquery
  = ([TotalRecovered] / [TotalCases]) * 100

- **Optional: Wave Grouping (Custom Reporting Periods)**  
  ```powerquery
  = if [TotalCases] < 100000 then "Wave 1" 
  else if [TotalCases] < 1000000 then "Wave 2" 
  else "Wave 3"

---

## 📌 Preview
![Dashboard Preview]

## 📌 Preview
![Dashboard Preview](https://github.com/Shagun-yadav/Interactive-Dashboard-Covid-19-/blob/main/Covid-19%20Dashboard.png)
