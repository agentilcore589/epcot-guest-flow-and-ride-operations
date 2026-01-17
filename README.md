# EPCOT Guest Flow Analysis

This project explores simulated EPCOT guest movement data to understand how visitors move between park zones, how congestion changes throughout the day, and how operational factors like wait times relate to guest experience metrics.

The analysis is **descriptive**, with a focus on identifying patterns that could inform crowd management and guest experience decisions.

---

## Project Overview

Using simulated event-level data, this analysis examines:

- Guest movement between EPCOT zones
- Zone-level congestion by time of day
- Ride wait time patterns
- Relationships between wait time, fun score, and frustration score
- Differences in guest experience across festivals

The project combines **Python-based exploratory data analysis** with a **Power BI dashboard** to demonstrate both analytical reasoning and clear communication of results.

---

## Data Description

The dataset represents simulated guest activity within EPCOT and includes:

- Timestamps for movement and ride events
- Source and destination zones (`zoneS`, `zoneD`)
- Ride names and actual wait times
- Guest experience metrics (fun score, frustration score)
- Festival identifiers

> **Note:** This dataset is simulated and is used for educational and portfolio purposes only.

---

## Analysis Highlights

### Zone Congestion
- Guest movement patterns vary significantly by both **zone** and **time of day**
- Certain zones experience sustained inflow across multiple hours, while others show short but intense peaks

### Ride Wait Times
- A small set of attractions consistently generates the highest average wait times
- These rides represent meaningful time costs for guests, especially during peak periods

### Guest Experience Metrics
- Longer wait times are generally associated with higher frustration, though the relationship is not perfectly linear
- Fun and frustration scores reflect a multi-dimensional guest experience rather than a simple tradeoff

### Festival Comparisons
- Guest experience metrics vary across festivals
- Some festivals show more consistent fun scores, while others exhibit wider variability

---

## Tools & Technologies

- **Python** (pandas, numpy, matplotlib, seaborn)
- **Jupyter Notebook** for exploratory analysis
- **Power BI** for dashboard visualization
- **GitHub** for version control and portfolio presentation

---

## Files in This Repository

- `epcot_guest_flow_analysis.ipynb`  
  Main exploratory data analysis notebook with visualizations and interpretations

- `epcot_guest_flow_large_stable.csv`  
  Simulated EPCOT guest flow dataset

- `Epcot.pbix`  
  Power BI dashboard file

---

## Key Takeaways

This project demonstrates how combining movement data, operational metrics, and guest experience indicators can provide a more complete picture of behavior within a theme park environment.

Rather than predicting outcomes, the analysis focuses on **understanding patterns** that could support operational awareness and experience-focused decision-making.

---

## Author

**Andrew Gentilcore**  
Business Analytics student at the University of Tennessee, Knoxville  
Graduating May 2026  
