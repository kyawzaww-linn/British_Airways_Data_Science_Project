# 📊 Lounge Utilization Analysis: Findings & Recommendations

## 1. Executive Summary
This report details the methodology and results of the predictive model built to estimate British Airways lounge usage. By analyzing historical flight data, we have identified key passenger traffic patterns that will assist in staffing optimization.

## 2. Key Insights & Data Patterns
Our analysis of the `lounge_lookup_table.csv` reveals distinct regional variances in passenger eligibility.

### Region with Highest Utilization: Europe
* **Total Eligibility:** **~21.6%** (Highest of all regions)
* **Driver:** This high percentage is driven largely by the **Tier 3** segment (16.85%), suggesting a high volume of business commuters or Club Europe passengers on short-haul routes.
* **Operational Note:** Despite the shorter flight duration, the *density* of eligible passengers is highest here, meaning morning "business waves" to European capitals will cause rapid spikes in lounge occupancy.

### Region with Moderate Utilization: North America
* **Total Eligibility:** **~14.4%**
* **Observation:** While North America is a premium market, the utilization percentage is lower than Europe.
* **Justification:** Long-haul aircraft (e.g., A380, B777) have large Economy cabins that dilute the overall percentage of eligible passengers per flight compared to smaller short-haul aircraft.

### Lowest Utilization Regions: Asia & Middle East
* **Total Eligibility:** **~14.0%**
* **Implication:** Flights to these regions have the lowest probability per-passenger of requiring lounge access. However, given the large aircraft size, the *absolute* number of passengers may still be high, even if the *percentage* is lower.

## 3. The Solution: Predictive Lookup Table
We generated a probabilistic lookup table (`outputs/lounge_lookup_table.csv`) to predict lounge demand.

| Region | Tier 1 (Gold) | Tier 2 (Silver) | Tier 3 (Bronze/Club) | **Total Probability** |
| :--- | :--- | :--- | :--- | :--- |
| **Europe** | 0.34% | 4.40% | 16.85% | **21.59%** |
| **North America** | 0.22% | 2.95% | 11.23% | **14.40%** |
| **Middle East** | 0.22% | 2.85% | 10.90% | **13.97%** |
| **Asia** | 0.21% | 2.86% | 10.98% | **14.05%** |

## 4. Strategic Recommendations
Based on the data, we recommend the following:
1.  **Staffing for European Waves:** Allocate maximum staff during early morning departure windows (06:00 - 09:00) when European business traffic is at its peak.
2.  **Inventory Management:** While long-haul flights consume more food/drink per person, the *frequency* of European flights means the "grab-and-go" stations (coffee, pastries) will see the highest turnover and need rapid restocking.
3.  **Space Planning:** Since European passengers often have shorter dwell times (quick pre-flight coffee vs. full meal), ensure there is ample "short-stay" seating (bar stools, high tops) available in the main lounge areas.