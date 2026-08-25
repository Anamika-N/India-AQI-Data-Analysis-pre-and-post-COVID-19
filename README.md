# Analyzing Air Quality Index (AQI) in India

> **Self Project** | Python · Pandas · NumPy · Plotly · EDA · Geospatial Analysis

---

## Overview

An exploratory data analysis of India's air quality from 2015 to 2020, covering hundreds of monitoring stations across major cities and states. The project integrates multi-source datasets — city-level and station-level AQI, hourly and daily granularity, and temperature data — to uncover pollution trends, spatial patterns, and the measurable impact of the COVID-19 lockdown on air quality.

---

## Datasets

| File | Description |
|---|---|
| `city_day.csv` | Daily AQI per city |
| `city_hour.csv` | Hourly AQI per city |
| `station_day.csv` | Daily AQI per monitoring station |
| `station_hour.csv` | Hourly AQI per monitoring station |
| `stations.csv` | Station metadata (name, location) |
| `city_temperature.csv` | Daily temperature for major Indian cities |

Source: [Air Quality Data in India — Kaggle](https://www.kaggle.com/datasets/rohanrao/air-quality-data-in-india)

**Pollutants covered:** PM2.5, PM10, NO2, SO2, CO, O3, NH3, NOx, Benzene, Toluene, Xylene

---

## AQI Categories

| AQI Range | Remark | Health Impact |
|---|---|---|
| 0–50 | Good | Minimal |
| 51–100 | Satisfactory | Minor discomfort to sensitive groups |
| 101–200 | Moderate | Breathing discomfort (asthma/heart patients) |
| 201–300 | Poor | Breathing discomfort on prolonged exposure |
| 301–400 | Very Poor | Respiratory illness |
| 401–500 | Severe | Serious health effects |

---

## Analysis Sections

### 1. AQI Monitoring Stations in India
- Interactive Plotly map of all monitoring stations with coordinates
- Station coverage across states and pollution control boards (DPCC, CPCB, MPCB, etc.)

### 2. Impact of COVID-19 Lockdown on AQI
- Pre- vs. post-lockdown AQI comparison across major cities
- Post-lockdown AQI levels fell to ≤100 (Good/Satisfactory) across monitored stations, compared to substantially higher pre-lockdown levels
- Time-series plots showing the lockdown effect on PM2.5, PM10, and overall AQI

### 3. Condition of Metropolitan Cities
- City-level AQI trends for Delhi, Mumbai, Bengaluru, Kolkata, Chennai, Hyderabad
- Pollutant-wise breakdown and seasonal variation
- Heatmaps of pollutant concentrations across cities

### 4. Yearly Analysis (2015–2020)
- Year-over-year AQI trends aggregated at daily, monthly, and hourly intervals
- Temporal feature engineering: year, month, week, day, hour

---

## Key Findings

- Post-lockdown (April–May 2020) AQI fell to the **Good/Satisfactory** range (≤100) across most monitored stations, a dramatic improvement over pre-lockdown levels
- Delhi consistently records the highest AQI among metropolitan cities, driven by PM2.5 and PM10
- AQI follows a strong seasonal pattern — worst in winter (Oct–Jan) due to crop burning and meteorological conditions, best in monsoon months

---

## Project Structure

```
india-aqi-analysis/
├── studying-india-s-aqi.ipynb   # Full analysis notebook
├── requirements.txt
└── README.md
```

### Data path (Kaggle)
```
/kaggle/input/air-quality-data-in-india/
/kaggle/input/daily-temperature-of-major-cities/
```
Update paths in the notebook if running locally.

---

## Setup

```bash
pip install -r requirements.txt
```

Open `studying-india-s-aqi.ipynb` in Jupyter or run directly on [Kaggle](https://www.kaggle.com/code/anshuls235/studying-india-s-aqi).

> **Note:** The notebook uses a Google Maps API key and Mapbox token (via Kaggle Secrets) for the interactive station map. Replace with your own keys or use the pre-computed station coordinates dictionary already embedded in the notebook.
