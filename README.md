# 🌤️ DSTC-5082: Hybrid Weather Forecasting using LSTM and Multi-Source APIs

This project aims to improve short-term weather prediction by integrating multiple meteorological data sources and applying a deep learning model (LSTM). By combining data from OpenWeather and NASA POWER APIs, we overcome the limitations of relying on a single source and enhance the robustness of forecasting results.

## 📌 Table of Contents
- [Overview](#overview)
- [Problem Statement](#problem-statement)
- [Data Sources](#data-sources)
- [Data Preparation](#data-preparation)
- [Modeling](#modeling)
- [Results](#results)
- [How to Run](#how-to-run)
- [Dependencies](#dependencies)
- [Contributors](#contributors)
- [License](#license)

---

## 📖 Overview

Weather forecasts are vital for planning, safety, agriculture, and energy management. However, single-source models suffer from missing or inconsistent data. This project proposes a hybrid LSTM-based approach to integrate and learn from multiple weather data sources.

---

## ❓ Problem Statement

Traditional weather models depend heavily on a single API, making them prone to inaccuracies. Our goal is to explore whether multi-source data fusion can:

- Reduce prediction error
- Increase reliability
- Capture complex weather trends more accurately

---

## 🌐 Data Sources

- **OpenWeather API**  
  Provides temperature, humidity, wind speed, pressure, etc.
  
- **NASA POWER API**  
  Provides irradiance, precipitation, longwave/shortwave radiation, and environmental variables.

---

## 🧹 Data Preparation

- Cleaned and standardized timestamp formats
- Handled missing data using interpolation
- Aggregated overlapping variables using median/mean
- Merged two datasets based on time index
- Selected important features for model input

---

## 🧠 Modeling

- Used **LSTM (Long Short-Term Memory)** network for time series forecasting
- Trained on combined dataset to predict temperature
- Evaluated model using:
  - Mean Squared Error (MSE)
  - Mean Absolute Error (MAE)
  - R² Score

---

## 📊 Results

| Model Type           | Data Source             | MSE     | MAE     | R²     |
|----------------------|--------------------------|---------|---------|--------|
| LSTM (Single Source) | OpenWeather              | 0.9059  | 0.6863  | 0.9911 |
| LSTM (Multi-Source)  | OpenWeather + NASA POWER | **0.2441**  | **0.3728**  | **0.9971** |

✅ The LSTM model trained with multi-source data showed significant improvement in accuracy and reduced error rates.

---

## ▶️ How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/vjkumargeesala/DSTC-5082
   cd DSTC-5082
