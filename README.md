# EPCOT Guest Flow & Ride Operations Analysis

This project explores simulated EPCOT guest movement data to understand how visitors circulate through park zones, which attractions generate the most wait time, how queue signage accuracy affects guest experience, and how outcomes shift across festivals and ticket types.

Built as a portfolio project targeting theme park and entertainment analytics, with Disney Parks operations and guest experience roles as the primary focus.

---

## Project Goals

- Identify when and where congestion builds across EPCOT's 15 zones
- Surface which attractions create the highest time cost for guests
- Quantify how well posted wait times reflect actual guest experience
- Diagnose a confounding effect between wait time and fun score that appears in aggregate data
- Segment guest behavior by ticket type (standard, park hopper, annual pass)
- Measure how festival context shifts experience outcomes

---

## Dataset

The dataset is synthetic and structurally representative. It was built to mirror realistic EPCOT guest dynamics, including ride demand hierarchy, time-of-day crowd curves, posted vs. actual wait distributions, and experience score drivers. No proprietary Disney data was used.

| Field | Description |
|---|---|
| `guest_id` | Unique guest identifier |
| `event_timestamp` | Datetime of the movement or ride event |
| `from_zone` / `to_zone` | Origin and destination park zone |
| `ride_name` / `ride_category` | Attraction and category (null for movement-only events) |
| `posted_wait_min` | Signage wait time at queue entry |
| `actual_wait_min` | True wait time experienced by the guest |
| `ride_duration_min` | Ride length in minutes |
| `crowd_level` | Crowd density estimate on a 1 to 10 scale |
| `temperature_f` | Ambient temperature in Fahrenheit |
| `weather` | Conditions: clear, cloudy, light_rain, or storm |
| `festival` | Active festival: Flower and Garden, Food and Wine, Festival of the Arts, or none |
| `party_size` | Guest group size |
| `ticket_type` | standard, park_hopper, or annual_pass |
| `fun_score` / `frustration_score` | Simulated guest experience ratings on a 1 to 10 scale |

**~80,000 records | 15 zones | 14 attractions | 4 festivals | 3 ticket types | ~5,000 unique guests**

Key structural properties built into the dataset:

- Ride demand is skewed so that Guardians of the Galaxy draws roughly 7x the visits of Reflections of China, consistent with actual EPCOT demand patterns
- Crowd level follows a realistic bell curve peaking around 1pm with a secondary evening bump
- Posted times are overstated by about 8% on average, which is how parks tend to engineer positive surprises
- Annual passholders arrive later and travel in smaller groups than standard guests
- Wait times scale correctly with crowd level, from around 25 minutes at low crowds to 60 minutes at peak
- Experience scores have independent drivers beyond wait time, including ride quality and expectation gaps

---

## Analysis Highlights

### Zone Congestion and Flow
Guest density peaks between 11am and 2pm. World Discovery and World Nature see the widest inflow windows due to their high-demand attractions. World Showcase traffic builds through the afternoon as guests move through pavilions in sequence. The most common zone transitions cluster along the World Showcase corridor, which reflects how the park layout naturally funnels guest movement.

### Ride Wait Times
Guardians of the Galaxy, Frozen Ever After, and Remy's Ratatouille Adventure generate the highest average waits, with wide standard deviations that make them hard to plan around. Lower-demand rides like Spaceship Earth and Gran Fiesta Tour are more predictable regardless of crowd conditions.

### Posted vs. Actual Wait Accuracy
On average, guests wait slightly less than posted, which is intentional. Wait delta (actual minus posted) varies by ride and is one of the stronger predictors of guest frustration when it goes negative (guests waiting longer than the sign indicated).

### Ride Quality Confounding
At the aggregate level, wait time and fun score appear positively correlated. This is a confounding artifact: better rides attract more guests, which drives up both wait times and fun scores simultaneously. Within any individual ride, longer waits consistently reduce fun scores. The notebook explicitly diagnoses this as a Simpson's Paradox analog and shows the contrast between aggregate and within-ride analysis.

### Ticket Type Segmentation
Annual passholders arrive later, move in smaller groups, and behave differently than first-time or infrequent visitors. Park hoppers arrive latest. Standard guests skew toward early arrival and higher event counts per day. Treating all ticket types the same in a crowd model would miss real behavioral differences.

### Festival Comparison
Food and Wine draws the heaviest crowds and the highest frustration scores. Flower and Garden produces the most consistent guest experience. Festival of the Arts sits between the two on crowd density and score variability.

---

## Tools and Technologies

- Python (pandas, numpy, matplotlib, seaborn, scipy)
- Jupyter Notebook for exploratory analysis and visualization
- Power BI for interactive dashboard (Epcot.pbix included)
- GitHub for version control and portfolio hosting

---

## Repository Structure

```
epcot-guest-flow-and-ride-operations/
├── Epcot_Guest_Flow_Analysis.ipynb     # Main EDA notebook (13 sections)
├── epcot_guest_flow_large_stable.csv   # Synthetic guest flow dataset
├── Epcot.pbix                           # Power BI dashboard
├── requirements.txt                     # Python dependencies
└── README.md
```

---

## Getting Started

```bash
git clone https://github.com/agentilcore589/epcot-guest-flow-and-ride-operations.git
cd epcot-guest-flow-and-ride-operations
pip install -r requirements.txt
jupyter notebook Epcot_Guest_Flow_Analysis.ipynb
```

The CSV needs to be in the same folder as the notebook. No API keys or external data sources required.

---

## Potential Extensions

- Train a regression or gradient boosting model to predict frustration score using wait delta, crowd level, festival, and ticket type
- Cluster guests by movement pattern and experience profile to identify behavioral archetypes
- Forecast zone-level congestion by hour to support staffing and routing decisions
- Add ticket type and festival filters to the Power BI dashboard for interactive exploration
- Quantify the weather impact on zone selection and experience scores

---

## Author

**Andrew Gentilcore**  
B.S. Business Analytics, University of Tennessee, Knoxville (May 2026)  
Minor in Data Science | Collateral in Information Management  

[GitHub](https://github.com/agentilcore589) · [LinkedIn](https://linkedin.com/in/andrewgentilcore)
