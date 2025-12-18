Project Overview

This project analyzes guest behavior and operational performance at EPCOT by combining zone-to-zone guest flow data with attraction wait-time analytics. The goal is to understand how guests move throughout the park, identify circulation hubs, and evaluate ride efficiency and wait-time accuracy across different attraction categories.

Guest circulation patterns are evaluated using matrix-based heatmaps and network visualizations, while ride operations are analyzed by comparing posted vs. actual wait times and calculating efficiency metrics.

Note on data:

The guest flow data used in this project is a synthetic, structurally representative dataset designed to mirror realistic EPCOT circulation patterns. This allows analytical techniques to be demonstrated without access to proprietary guest data.

Key Questions

Which EPCOT zones act as major circulation hubs?

Are guest movement patterns directionally asymmetric between zones?

How accurately do posted wait times reflect actual guest experience?

How does ride efficiency vary by attraction category (thrill, family, show)?

Guest Flow Analysis

Methods

Zone-to-zone flow matrices

Heatmaps with conditional formatting

Sankey diagram for directional connectivity

Why multiple visuals?

Because the guest flow dataset is stabilized at one record per zone-to-zone connection, magnitude is best analyzed using heatmaps, while the Sankey diagram is used to illustrate structural connectivity and directional pathways rather than absolute volume.

Insights

Central World Showcase pavilions (e.g., France, United Kingdom, Germany, Japan) act as major circulation hubs.

Peripheral zones show lower overall connectivity, indicating more destination-driven visits.

Directional asymmetries suggest guests are more likely to exit certain pavilions than enter them, which has implications for crowd management and staffing.

Ride Operations & Wait-Time Analysis

Methods

Posted vs. actual wait time comparison

Ride efficiency score calculation

Category-level aggregation (thrill, family, show)

Ranking of attractions by average actual wait time

Insights

Posted wait times generally track actual waits but diverge more for high-demand thrill attractions.

Ride efficiency varies substantially by category, with some attractions consistently outperforming others in managing queue times.

Certain rides show persistently high average actual waits, highlighting opportunities for operational optimization or guest communication improvements.

Visualizations Included

Zone-to-zone guest flow heatmaps

Directional Sankey diagram (structural connectivity)

Posted vs. actual wait time scatter plot

Ride efficiency bar charts

Average wait time rankings by attraction

All visuals were built in Power BI with interactive filters for exploration.

Tools & Technologies

Power BI (visualization, DAX, dashboarding)

Python / Pandas (data preparation, optional preprocessing)

Synthetic data modeling for guest flow simulation

Why This Project Matters

This analysis demonstrates how to:

Work with limited or sensitive data responsibly

Choose the correct visualization based on data grain

Avoid misleading analytics

Translate technical findings into operational insights

Communicate assumptions clearly and professionally

These are core skills for analytics roles in theme parks, entertainment, and operations strategy.
