# 🚓 Tactical Crime Analysis Dashboard Using Power BI

A comprehensive Power BI project designed to analyse crime patterns, identify hotspots, study offender–victim behaviour, and assist law-enforcement decision-making.
This dashboard converts raw crime data into actionable insights for operational and tactical policing.

![image](https://github.com/Debdatta7/Tactical-Crime-Analysis/blob/main/Screenshot%20(100).png)
## 📌 Problem Statement

# 🎯 Project Objectives

This project aims to build an interactive Power BI dashboard to:

* Analyse crime trends, hotspots, and behavioural patterns
* Identify high-risk locations and high-crime time windows
* Track solved vs. unsolved cases and resolution efficiency
* Provide demographic insights for victims and offenders


🗂️ Dataset Description

Primary Tables Used:
- Crimes: Crime ID, Date, Time, Latitude, Longitude, Crime Type ID, Resolved, People Involved
- Crime Types: Crime category names
- Crime Person: Linking table (Crime ↔ People)
- People: Age, Gender, Demographic details
- Crime Roles: Victim, Offender, Witness
- Calendar Table: Created using DAX for date intelligence

These tables collectively form a relational model to support advanced analysis.

# 🔧 Data Preparation & Transformations
Step 1 — Data Cleaning

1. Validated datatypes
2. Extracted time from datetime column
3. Created Calendar table using DAX:
CALENDAR ( MIN(Crimes[Crime Date]), MAX(Crimes[Crime Date]) )
4. Added derived columns: day name, weekday/weekend, start of month
5. Extracted age from People table
6. Rounded latitude/longitude for zone grouping
7. Created Location Zones using grouped coordinates

Step 2 — Data Modelling

1. Built a star schema using fact and dimension tables
2. Connected Calendar, Crime Types, People, and Roles into the model


Step 3 — DAX Measures

Key measures created include:

- Total Crimes, Resolved Crimes, Unresolved Crimes, Resolution %
- Total People, Male %, Female %

- Crime count by role

- Crime type totals

- Previous Month, MoM, YoY comparisons


# 📊 Dashboard Pages
📍 Page 1 — Crime Overview

![image](https://github.com/Debdatta7/Tactical-Crime-Analysis/blob/main/2.JPG)

⏱ Page 2 — Temporal Analysis




🗺 Page 3 — Crime Hotspot Analysis (Azure Map)




🧑‍🤝‍🧑 Page 4 — Victim & Offender Analysis




🚀 Conclusion

This tactical crime analysis dashboard empowers agencies with data-driven insights into crime behaviour, hotspots, timelines, and demographic profiles.
It enables faster decision-making, resource allocation, and operational planning.
