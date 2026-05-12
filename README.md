# Dakar Air Quality Analysis

Analysis of air quality in Dakar, Senegal using real-time data from the OpenWeatherMap API.

## Motivation

Dakar is one of the most polluted cities in West Africa, regularly affected by Saharan dust storms and urban pollution. Yet very little data analysis exists on this topic. This project collects, processes and visualizes real air quality data to understand pollution patterns in the city.

## What This Project Does

- Fetches real-time and historical air quality data from OpenWeatherMap API
- Analyzes 5 key pollutants : PM10, PM2.5, O3, NO2, SO2
- Produces visualizations showing pollution trends over time
- Compares measured values against WHO safety thresholds

## Key Findings

- PM10 reached 160.49 ug/m3 on May 12 2026, more than 3x the WHO threshold of 50
- Air quality was above WHO PM10 limit 14% of the time over the past 5 days
- A sharp spike in all particulate matter was recorded on May 12, likely caused by a Saharan dust event

## Tech Stack

- Python 3.14
- Pandas — data manipulation
- Matplotlib / Seaborn — visualizations
- Requests — API calls
- Python-dotenv — environment variables management

## Project Structure

dakar-air-quality-analysis/
├── data/                        # CSV data files
├── notebooks/
│   └── air_quality_dakar.ipynb  # Main analysis notebook
├── visuals/                     # Generated charts
├── .env                         # API key (not tracked)
└── README.md

## How to Run

1. Clone this repository
2. Create a virtual environment and install dependencies
```bash
pip install pandas requests matplotlib seaborn plotly python-dotenv
```
3. Get a free API key from openweathermap.org
4. Create a `.env` file with `API_KEY=your_key_here`
5. Run the notebook `notebooks/air_quality_dakar.ipynb`

## Data Source

OpenWeatherMap Air Pollution API — https://openweathermap.org/api/air-pollution

Coordinates used : 14.6937 N, 17.4441 W (Dakar, Senegal)