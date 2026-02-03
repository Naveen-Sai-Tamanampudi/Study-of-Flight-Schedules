# US Domestic Flight Analysis Project

## Project Overview
This project explores US domestic flight data between 2019 and 2023. While 33.66 million flights occurred in the US during this period, this analysis focuses on optimizing data architecture and visualization using a subset of records to handle complex flight statuses like cancellations and diversions.

---

## Project Version-1: Data Normalization & Cleaning
The focus of this version was addressing the "sparse table" problem. Since cancelled flights lack arrival times and completed flights lack cancellation codes, keeping everything in one table caused significant space wastage and "null" bloat.

### Technical Implementation:
* **Schema Optimization:** Divided the 100K record dataset (32 columns) into 3 normalized tables to eliminate redundancy and handle different flight statuses efficiently.
* **ETL Workflow:** 1. Used **Power Query** to split and clean data, saving the state via **Power BI Helper**.
    2. Conducted **EDA** and outlier removal using **Python** (`EDA.ipynb`).
    3. Modeled and visualized data in **Power BI** (`Hypothesis Visualizations.ipynb`).
* **Advanced Analytics:** Created complex calculated columns and measures using **DAX**.



---

## Project Version-2: Scaling & UI/UX Revamp
I revamped the project to handle a larger scale and provide a more polished, application-like experience.

### Key Improvements:
* **Increased Scale:** Scaled the analysis to a **3 million record sample**, performing all processing within Power BI.
* **SQL Integration:** Uploaded the dataset to a **SQL Server** to bypass the 1GB Power BI import limit, ensuring a stable and professional data connection.
* **Time Intelligence:** Built a **Rolling Calendar** to enable accurate year-over-year and trend analysis.
* **Web-App Interface:** Developed a 3-page report utilizing **Bookmarks**, **Drill-throughs**, and **Slicers** to mimic a functional web application.
* **Cloud Deployment:** Deployed the final report to **Power BI Service** for cross-collaboration.

---

## 📊 View Report
[**Interactive Power BI Dashboard**](https://app.powerbi.com/view?r=eyJrIjoiMDFlOTgwZGItNWRiNi00MmE3LWFjZmItNDRiNjkzMzMxYzA1IiwidCI6IjcwZGUxOTkyLTA3YzYtNDgwZi1hMzE4LWExYWZjYmEwMzk4MyIsImMiOjN9&pageName=ReportSection)

---

## Tech Stack
* **Tools:** Power BI Desktop, Power BI Service, Power BI Helper
* **Database:** Microsoft SQL Server
* **Languages:** DAX, Python (Pandas), SQL
