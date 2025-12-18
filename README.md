# epcot-guest-flow-and-ride-operations
The guest flow data used in this project is a synthetic, structurally representative dataset designed to mirror realistic circulation patterns within EPCOT, allowing analytical techniques to be demonstrated without access to proprietary guest data.

## Guest Flow Analysis
Guest circulation between EPCOT zones was examined using heatmaps and a Sankey
diagram. Heatmaps capture the intensity of movement between zones, while the
Sankey diagram illustrates directional connectivity.

Because the flow dataset is stabilized at one record per zone-to-zone connection,
magnitude is analyzed via matrix-based visualizations rather than Sankey width.

## Ride Operations Analysis
Ride performance was evaluated by comparing posted versus actual wait times,
calculating ride efficiency scores, and analyzing differences across attraction
categories (thrill, family, show).

## Key Insights
- Central World Showcase pavilions act as major circulation hubs.
- Guest movement shows directional asymmetry across zones.
- Posted wait times systematically differ from actual waits, especially for
  high-demand thrill attractions.
- Ride efficiency varies substantially across categories.
