# Deloitte-Data-Analytics-Job-Simulation-Forage
Completed Deloitte Australia's Data Analytics Virtual Internship on Forage – built Tableau dashboards and conducted forensic pay equity analysis using Excel.

# Deloitte Australia Data Analytics Virtual Internship (Forage)

This repository contains my completed project work from the **Deloitte Australia Data Analytics Virtual Experience** hosted on [Forage](https://www.theforage.com/). The program simulates real-world consulting tasks focusing on data visualization, business insights, and ethical analytics.

---

## 📁 Project Tasks Overview

### Task 1: **Telemetry Data Analysis with Tableau**

#### 🔹 Background

The client, **Daikibo Industrials**, operates four factories:

* Meiyo (Tokyo, Japan)
* Seiko (Osaka, Japan)
* Berlin (Germany)
* Shenzhen (China)

Each site runs 9 machine types that report telemetry data every 10 minutes. Data was collected for **May 2021** and shared as a unified JSON file.

#### 🔍 Objective

The client needed answers to:

1. Which factory experienced the most machine breakdowns?
2. Which machine types failed most often in that factory?

#### 🛠️ Steps & Implementation

**Step 1:** Import the JSON telemetry data into Tableau.

**Step 2:** Create a calculated field to measure machine downtime:

```tableau
IF [Status] = "Unhealthy" THEN 10 ELSE 0 END
```

Each 'Unhealthy' message corresponds to 10 minutes of downtime.

**Step 3:** Build a visualization for **Downtime by Factory** (Bar chart).

**Step 4:** Build a visualization for **Downtime by Machine** within each factory.

**Step 5:** Combine the visualizations into a dashboard. Use a filter (funnel icon) on the factory bar chart to dynamically update the machine chart based on selection.

#### 📊 Outcome

* **Daikibo Meiyo (Tokyo)** had the highest overall downtime.
* Machines **Type 4** and **Type 7** were the most problematic in Meiyo.
* Enabled operational insight into maintenance priorities.

---

### Task 2: **Forensic Pay Equality Analysis using Excel**

#### 🔹 Background

Daikibo received internal complaints regarding **gender pay inequality**. A forensic team developed an algorithm to assign **Equality Scores** (-100 to +100) for each role in each factory.

#### 🧩 Provided Dataset Columns:

1. Factory
2. Job Role
3. Equality Score (ideal = 0)

#### 📝 Objective

Classify roles based on their Equality Score into:

* **Fair**: between -10 and +10
* **Unfair**: between -20 to -11 or +11 to +20
* **Highly Discriminative**: < -20 or > +20

#### 📐 Solution

Created a new column in Excel using:

```excel
=IF(ABS(C2)<=10,"Fair",IF(ABS(C2)<=20,"Unfair","Highly Discriminative"))
```

This logic ensures both underpaying and overpaying inequalities are treated equally.

#### 📊 Insights

* **Operational Support** roles showed high levels of discrimination in some factories.
* **Engineering roles** were largely rated as fair.
* **Meiyo factory** had the most "Highly Discriminative" job roles.

---

## 💼 Key Skills Demonstrated

* Tableau Public (dashboarding, calculated fields, interactivity)
* Excel (formulas, classification logic)
* Data storytelling
* Ethical data analysis
* Real-world business simulation

---

## 📎 Program Link

🔗 [Deloitte Australia Data Analytics Simulation](https://www.theforage.com/simulations/deloitte-au/data-analytics-s5zy)

---

## 📂 Repo Contents

* `/Screenshots` – Tableau dashboards and Excel classification images
* `equality_classification.xlsx` – Processed Excel file
* `telemetry_dashboard.twbx` – Tableau workbook
* `README.md` – Project write-up

---

## 📢 Author

**Kritika Mishra**
Feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/kritika-mishra-578574317/) or reach out for collaboration opportunities!
