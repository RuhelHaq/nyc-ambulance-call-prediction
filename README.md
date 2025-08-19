
# NYC Ambulance Call Volume Prediction

Predicting daily ambulance call demand across New York City's boroughs using EMS dispatch data, weather conditions, and holiday indicators.

---

##  Project Objective

The goal of this project is to forecast **daily ambulance call volume** in each of NYC's five boroughs. Accurate predictions can help improve
**EMS resource allocation**, **staffing**, and **response times**, especially during high-demand periods.

---

##  Context

New York City’s EMS handles thousands of 911 calls daily. These calls vary significantly depending on:

- **Time factors** (weekday, weekend, holidays)
- **Weather conditions** (temperature, snowfall, rain)
- **Geographic location** (borough-specific demand)

By building a machine learning model, this project aims to predict call volume patterns using historical data and external features.

---

## 📁 Repository Structure

```bash
├── README.md                     # Project overview and documentation
├── data/
│   ├── daily_ambulance_calls.csv       # Aggregated EMS data (daily borough-level call volume)
│   ├── nyc_boroughs_weather.csv          # Daily weather data for NYC
├── 1_data_wrangling.ipynb        # Load & clean EMS data, add weather & holiday features
├── 2_eda.ipynb                   # Visual exploration of trends, patterns, borough-level insights
├── 3_preprocessing.ipynb         # Final feature selection, encoding, normalization, train/test split
├── 4_modeling.ipynb              # Training & evaluating models (Linear Regression, RF, XGBoost)
├── 5_report.md                   # Written summary of methodology, results, and key findings
├── 6_presentation_slides.pdf     # Presentation slides for stakeholders
├── assets/                       # Images or visualizations used in report/README
└── requirements.txt              # Python package dependencies


## Data Sources
EMS Dispatch Data (Jan 1 – Apr 15, 2025)
NYC Open Data API – EMS Incident Dispatch
url = "https://data.cityofnewyork.us/resource/76xm-jjuj.json"
⮑ 500,000 rows retrieved via API, aggregated to daily call counts.
Weather Data
Daily NYC weather observations (temperature, precipitation, snowfall, etc.)
Holiday Calendar
U.S. federal and NY state holidays, used to flag public/non-working days.
