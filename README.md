# Load and Weather Data Analysis (2024)

This repository provides a comprehensive analysis of the standard load profile from a local utility, in relation to weather conditions fetched from Open-Meteo for the year 2024. By merging high-resolution load data with detailed weather metrics, the project uncovers patterns, trends, and insights relevant to energy management and forecasting. Both datasets are open-sourced and available for forecasting and understanding the load consumption of a town.

## Project Structure

- `data_analysis.ipynb`: Main notebook containing all data processing, analysis, and visualization steps.
- `Netze-Strom-Lastprofil-SH0_2024 (2).csv`: Raw load profile data (15-minute intervals).
- `weather.csv`: Weather data (temperature, precipitation, radiation, humidity, etc.).
- `weather_fetch.ipynb`: (Optional) Notebook for fetching or preprocessing weather data.

## Data Overview

- **Load Data**: 15-minute interval electricity consumption for 2024.
- **Weather Data**: Temperature, precipitation, shortwave radiation, humidity, and more, aligned to the same time intervals.

## Analysis Workflow

1. **Data Loading & Cleaning**
   - Import and preprocess both datasets.
   - Handle missing values, time zone alignment, and ensure a perfect 15-minute grid.
   - Merge datasets on timestamp.
2. **Feature Engineering**
   - Add temporal features: hour, day, weekday, month, part of day, season, and weekend/weekday flags.
   - Calculate energy consumption per interval.
3. **Exploratory Data Analysis (EDA)**
   - Descriptive statistics for all variables.
   - Visualizations: histograms, time series, and grouped plots by temporal and weather features.
   - Analysis of load/energy consumption by part of day, weekday, month, and season.
   - Investigation of load behavior under extreme weather conditions.

## Key Findings

- **Load Profile**: Electricity load varies significantly throughout the year, with values ranging from ~11 kW to 56 kW. The distribution is right-skewed, with higher peaks in summer.
- **Temperature**: Ranges from -10.3°C to 31.6°C, with a mean around 9.6°C. Seasonal swings in temperature are reflected in load variations.
- **Precipitation & Snowfall**: Most intervals have no precipitation, but rare heavy rain events are observed. Snowfall is infrequent.
- **Shortwave Radiation**: Strong diurnal and seasonal patterns, with most intervals at low values and peaks during sunny days.
- **Relative Humidity**: Generally high, with most values between 70% and 100%.
- **Temporal Patterns**:
  - Weekdays and weekends show distinct daily load profiles.
  - Energy consumption is highest during the day, especially in the morning and evening.
  - Monthly and seasonal plots reveal higher loads in winter and summer, likely due to heating and cooling demands.
- **Extreme Weather**:
  - Load and energy consumption on days with extreme weather (hottest, coldest, wettest, driest, etc.) are visualized and compared.
  - Notable differences in load profiles are observed on these days, indicating weather sensitivity.

## Usage

1. Clone the repository.
2. Place the raw data files in the project directory.
3. Open `data_analysis.ipynb` in Jupyter or VS Code and run the cells sequentially.

## Requirements

- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn

Install dependencies with:

```
pip install pandas numpy matplotlib seaborn
```

## License

MIT License

---

### Summary of Findings

- The load profile exhibits strong daily, weekly, and seasonal cycles, with clear peaks during winter and summer.
- Temperature and shortwave radiation are key drivers of load variation, reflecting heating and cooling needs.
- Most precipitation and snowfall events are rare, but extreme weather days show distinct load patterns.
- Weekends and weekdays have different consumption profiles, with weekends generally showing lower daytime loads.
- Energy consumption is highest during the morning and evening parts of the day.
- The dataset is well-aligned and cleaned, enabling robust analysis of the interplay between weather and electricity demand.
