# NBA_shot_analytics_dashboard

## Overview
This project is an interactive Power BI dashboard designed to analyze NBA shot data for **defensive game planning.** It highlights opponent shot tendencies, efficiency by zone and distance, and shot selection patterns to help identify ways to limit high-value attempts and reduce overall scoring efficiency.

## Problem Statement
Current defensive coverage against league MVP **Nikola Jokić** allows frequent, high-efficiency shots in the paint, resulting in a Points per Attempt (PPA) of ~1.22 (above the league average of 1.15 PPA). The objective is to drive him out of his comfort zones and **lower his PPA to ~1.15** by adjusting the defensive scheme.

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
![NBA_Shot_Chart_Analytics(2023-2024)_page-0001](https://github.com/user-attachments/assets/4742c435-0472-4999-be90-2cd71b14670a)

### 1. Efficieny by Shot Distance
The dashboard shows a dramatic efficiency spike **inside 8 feet**, where he converts **67.5%** of attempts for **1.35 PPA.**  
As shots move outward, efficiency declines:  
- **8–16 ft:** 1.08 PPA  
- **16–24 ft:** 0.76 PPA  
- **24+ ft:** 1.12 PPA _(boosted by the extra value of threes, even at similar FG%)_  

### 2. Efficiency by Floor Zone
The **Center zone** is his most productive area at **1.25 PPA**. As he moves toward the sides, his efficiency dips — still good, but not nearly as punishing as the middle of the paint.

### 3. His Touch Shots drive his Scoring
Layups, hooks, and floaters make up more than **60%** of his attempts — and they’re also his most efficient shots., reinforcing the earlier distance and zone insights.

### 4. Jumpshots are Acceptable Outcomes
He can make them, but they don’t hurt you the same way. Standard jump shots, step‑backs, and fadeaways all come in well below his paint efficiency.

## Recommendations

### 1. Make his paint touches tougher
Jokić becomes extremely efficient when he catches the ball deep. Meet him early, fight for position, and **push his catches farther from the rim.**

### 2. Turn his drives and post-ups into mid‑range looks
When he’s outside the paint, his scoring drops. The goal is to keep him out of his comfort spots and force him to take more shots from the **mid‑post and elbow.**

### 3. Live with the jumpers
If he settles for face‑up jumpers or fadeaways, that’s a win. **Contest without fouling and trust the numbers** - those shots don’t beat you over time.

### 4. Take away his touch shots
Hooks, floaters, and short push shots are where he does the most damage. To disrupt those, **bring late help from the weak side** and **use length to bother his release.**
