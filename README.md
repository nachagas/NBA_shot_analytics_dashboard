# NBA_shot_analytics_dashboard
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA

## Overview
This project is an interactive Power BI dashboard designed to analyze NBA shot data for **defensive game planning.** It highlights opponent shot tendencies, efficiency by zone and distance, and shot selection patterns to help identify ways to limit high-value attempts and reduce overall scoring efficiency.

## Problem Statement
Current defensive coverage against league MVP **Nikola Jokić** allows frequent, high-efficiency shots in the paint, resulting in a Points per Attempt (PPA) of ~1.22. The goal is to disrupt his preferred areas by adjusting the defensive scheme, **lowering his PPA to ≤1.00.**

## Data
Shot‑level NBA data including shot coordinates, distances, zones, shot types, and make/miss outcomes. The dataset provides enough detail to analyze player tendencies, efficiency, and scoring patterns.  

Shot data was obtained from the open-source **NBA_Shots_04_25** repository by **Dom Samangy** on GitHub:  
https://github.com/DomSamangy/NBA_Shots_04_25?tab=readme-ov-file  
https://drive.google.com/file/d/1uktZ3wcE5670ZAR5c7MciMHbu8-zPMwM/view

## Methodology
### Data Preparation - Python & Pandas in Google Colab
- Filtered the dataset to include only the **2023–2024 NBA season,** significantly lowering memory usage and improving dashboard performance.
- Loaded the raw shot‑level dataset and inspected its structure to identify redundant or unnecessary fields.
- Dropped duplicate and non‑essential columns to reduce file size and improve processing efficiency.
- Normalized the dataset by separating repeated categorical information into **dimension tables**, reducing redundancy in the main fact table.



### Tools Used

## Insights

## Recommendations
