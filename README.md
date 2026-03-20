# NBA_shot_analytics_dashboard
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA

## Overview
This project is an interactive Power BI dashboard designed to analyze NBA shot data for **defensive game planning.** It highlights opponent shot tendencies, efficiency by zone and distance, and shot selection patterns to help identify ways to limit high-value attempts and reduce overall scoring efficiency.

## Problem Statement
Current defensive coverage against league MVP **Nikola Jokić** allows frequent, high-efficiency shots in the paint, resulting in a Points per Attempt (PPA) of ~1.22. The objective is to drive him out of his comfort zones and **lower his PPA to ≤1.00** by adjusting the defensive scheme.

## Data
Shot‑level NBA data including shot coordinates, distances, zones, shot types, and make/miss outcomes. The dataset provides enough detail to analyze player tendencies, efficiency, and scoring patterns.  

Shot data was obtained from the open-source **NBA_Shots_04_25** repository by **Dom Samangy** on GitHub:  
https://github.com/DomSamangy/NBA_Shots_04_25?tab=readme-ov-file  
https://drive.google.com/file/d/1uktZ3wcE5670ZAR5c7MciMHbu8-zPMwM/view

## Methodology
### Data Preparation - Python & Google Colab
- Filtered the dataset to include only the **2023–2024 NBA season,** significantly lowering memory usage and improving dashboard performance.
- Loaded the raw shot‑level dataset and inspected its structure to identify redundant or unnecessary fields.
- Dropped duplicate and non‑essential columns to reduce file size and improve processing efficiency.
- Normalized the dataset by separating repeated categorical information into **dimension tables**, reducing redundancy in the main fact table.

_Link:_ https://colab.research.google.com/drive/1rV-KDdv5cdVa5iJSXVyF8Jm3WuutfT8c?usp=sharing

### Data Modeling & Dashboard Development - Microsoft PowerBI/Power Query
- Imported the datasets into Power BI and constructed a **Data Model**, linking the fact table to dimension tables.
- Performed additional light cleaning and type adjustments in **Power Query**.
- Created DAX measures such as FG%, Points Per Attempt (PPA), Shot Frequency %, and total attempts.
- Designed interactive visuals such as bar charts, shot‑type breakdowns, and zone‑based efficiency views to support analysis.
<img width="766" height="721" alt="image" src="https://github.com/user-attachments/assets/7b30d24f-a0f1-4172-ab43-50bea93f06f6" />

## Insights
### 1. Overall Scoring Profile
Nikola Jokić’s overall efficiency is elite, posting **58.3% FG** and **1.22 PPA**. This immediately signals that his scoring value is driven by consistent access to high‑efficiency areas.

### 2. Efficieny by Shot Distance
The dashboard shows a dramatic efficiency spike **inside 8 feet**, where he converts **67.5%** of attempts for** 1.35 PPA.**  
As shots move outward, efficiency declines:  
• 	**8–16 ft:** 1.08 PPA  
• 	**16–24 ft:** 0.76 PPA  
• 	**24+ ft:** 1.12 PPA _(slightly higher due to the added scoring value of three‑point attempts, even at a similar FG%)_  
This confirms that deep paint touches are the engine of his scoring

## Recommendations
