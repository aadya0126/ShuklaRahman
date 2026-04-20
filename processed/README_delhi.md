---
license: apache-2.0
language:
- en
tags:
- climate
size_categories:
- 1M<n<10M
---
---

**Dataset Information:**

- **Name:** Processed Delhi Air Quality and Weather Data
- **Version:** 1.0.0
- **Description:**  
  This dataset contains **2.9M** rows of hourly weather and air quality data from multiple locations across Delhi, India, collected from March 2000 to November 2024. The data includes environmental parameters such as temperature, humidity, atmospheric pressure, wind speed, wind direction, and concentrations of pollutants (PM2.5, PM10, NO2, SO2, O3, CO), along with the corresponding Air Quality Index (AQI).  
  The data has been pre-processed for model training, including the following updates:
  - Rows with AQI values marked as `"-"` have been removed, as they accounted for 15% of the total dataset.
  - Missing values have been handled through various methods, including dropping, mean imputation, and nearest neighbor interpolation.
  - Centers responsible for missing data have been identified and documented.  
  **This processed dataset is specifically curated for model training. For alternative uses or visualizations, you may refer to the unprocessed version of the dataset**.(abhinavsarkar/delhi_air_quality_feature_store_processed.csv)

- **Citation:**  
  If you use this dataset in your research or project, please cite it as follows:  
  Abhinav. (2024). "Processed Delhi Air Quality and Weather Data". Dataset retrieved from Hugging Face.

- **Size:** 615 MB (Please verify and update with the actual dataset size).

---

**Dataset Fields:**

- **location_id:** Integer identifier for each location.
- **city:** The name of the city or specific location in Delhi.
- **event_timestamp:** The timestamp when the data was recorded, in ISO 8601 format.
- **temperature:** Ambient temperature in Celsius.
- **humidity:** Relative humidity as a percentage.
- **pressure:** Atmospheric pressure in hPa.
- **wind_speed:** Wind speed in m/s.
- **wind_direction:** Wind direction in degrees.
- **pm25:** Concentration of particulate matter with a diameter of 2.5 micrometers (µg/m³).
- **pm10:** Concentration of particulate matter with a diameter of 10 micrometers (µg/m³).
- **no2:** Concentration of nitrogen dioxide (µg/m³).
- **so2:** Concentration of sulfur dioxide (µg/m³).
- **o3:** Concentration of ozone (µg/m³).
- **co:** Concentration of carbon monoxide (µg/m³).
- **aqi:** Air Quality Index, a measure of the level of air pollution.

---

**Data Quality:**

- The dataset has been cleaned to remove rows with AQI values marked as `"-"`, which constituted 15% of the data.
- Missing values have been handled by dropping, using mean imputation, or applying nearest neighbor interpolation based on the specific data column.
- Centers responsible for sending incomplete or missing data have been identified and are documented.

---

**Usage with `load_dataset`:**

You can load this dataset using the Hugging Face `datasets` library with the following code:

```python
from datasets import load_dataset

dataset = load_dataset("abhinavsarkar/delhi_air_quality_feature_store_processed.csv")
```

---