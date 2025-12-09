# 🚓 Tactical Crime Analysis Dashboard Using Power BI

A comprehensive Power BI project designed to analyse crime patterns, identify hotspots, study offender–victim behaviour, and assist law-enforcement decision-making.
This dashboard converts raw crime data into actionable insights for operational and tactical policing.

## 📌 Problem Statement

Law enforcement agencies often struggle with:

* Identifying crime hotspots across the city
* Understanding peak crime timings (hour/day/month)
* Analysing crime types and spatial distribution
* Studying victim and offender demographics
* Tracking resolution performance and case outcomes
* Due to raw and unstructured crime data, agencies lack an integrated system to generate meaningful insights.

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


📊 Dashboard Pages
📍 Page 1 — Crime Overview

Provides a high-level summary of crime volume, resolution status, and trends.
Includes drill-through to view crime types.


⏱ Page 2 — Temporal Analysis

Analyses crime distribution by:

Hour of the day

Day of the week

Monthly and seasonal patterns


🗺 Page 3 — Crime Hotspot Analysis (Azure Map)

Identifies spatial crime clusters

Visualizes geographical hotspots based on grouped zones


🧑‍🤝‍🧑 Page 4 — Victim & Offender Analysis

Age and gender breakdown

Role-based crime involvement

High-risk demographic groups


📝 Key Findings
1. Crime Types

Violence & sexual offences are highest

Violent crimes show lower resolution rates compared to property crimes


2. Time-Based Patterns

Crimes peak between 9 PM – 2:45 AM

Lowest activity between 9 AM – 11:45 AM

Weekdays show higher crime activity

Seasonal spikes during summer months


3. Hotspot Analysis

A small number of zones contribute to most crimes

Hotspot patterns remain consistent across months


4. Demographics

Offenders mostly males aged 46–59

Victim profiles vary significantly across crime types


🚀 Conclusion

This tactical crime analysis dashboard empowers agencies with data-driven insights into crime behaviour, hotspots, timelines, and demographic profiles.
It enables faster decision-making, resource allocation, and operational planning.
