# QSR Demand Planning & S&OP Consensus Model

### Project Overview & Objective
This project demonstrates an end-to-end Sales and Operations Planning (S&OP) cycle for a Quick Service Restaurant (QSR) facing highly volatile daily demand. By bridging standard time-series forecasting with **human-in-the-loop market intelligence**, this model proves how qualitative consensus overrides can correct algorithmic blind spots to accurately predict daily inventory needs. 

The hybrid consensus approach successfully reduced out-of-sample forecast error (MAPE) by over **43%**, highlighting the critical value of business acumen in supply chain execution.

###  The Business Challenge
The QSR is located adjacent to a major movie theater and local festival grounds, making its foot traffic highly sensitive to localized external shocks:
1. **Theatrical Releases & Local Events:** Blockbuster premieres and local gatherings (e.g., food fests, town galas) create irregular demand spikes.
2. **Extreme Weather:** Regional snowstorms and heavy rainfall cause severe, immediate drop-offs in customer volume.

A standard seasonal time-series algorithm cannot predict these external shocks, leading to costly inventory stockouts on movie weekends and high food waste during severe weather.

###  The Solution & Methodology
I built a multi-stage forecasting tool in Excel to clean historical data, project a statistical baseline, and actively adjust for external drivers using S&OP principles:

1. **Data Hygiene & Outlier Cleansing (Z-Score):** Analyzed 731 days of raw POS transaction data, utilizing Z-scores to identify and quarantine historical anomalies (e.g., winter storm closures, state of emergency days) in a dedicated Exception Log.
2. **Statistical Baseline (Holt-Winters / ETS):** Generated a pure algorithmic forecast trained on 365 days of cleansed history (`FORECAST.ETS`) to capture the underlying 7-day weekly seasonality and general sales trends.
3. **Consensus S&OP Overrides:** Created an interactive 47-day forecasting dashboard where supply chain planners can log upcoming weather forecasts, movie schedules, and local events to apply percentage-based judgmental overrides to the statistical baseline.

###  Key Results & ROI (47-Day Backtest)
The model was tested on a 47-day out-of-sample horizon (Jul 20, 2026 – Sep 4, 2026) managing over $107,000 in revenue:
* **Algorithm-Only Error (Unadjusted ETS):** 17.0% MAPE (48.4 units of error/day)
* **Consensus Adjusted Error (Final S&OP Forecast):** **9.6% MAPE** (27.6 units of error/day)
* **Business Impact:** Eliminated nearly 21 units of daily inventory forecasting error, raising overall forecast accuracy to **90.4%**.

###  Tools & Skills Demonstrated
* **Advanced Excel:** `FORECAST.ETS`, Z-Score formulation, statistical standard deviation, dynamic arrays, and dashboard design.
* **Supply Chain Concepts:** Demand Planning, Sales and Operations Planning (S&OP), Outlier Cleansing, Judgmental Forecasting / Consensus Overrides, and Mean Absolute Percentage Error (MAPE) tracking.
* **Data Analytics:** Time-series smoothing, exception logging, and out-of-sample forecast backtesting.

## Project Screenshots

### Executive Dashboard
![Dashboard](Dashboard.png)

### Forecast Accuracy Tracker
![Forecast Accuracy](Forecast%20Accuracy.png)

### Multiple Inputs of Demand
![Multiple Inputs](Multiple%20Inputs%20of%20demand.png)



