# Renewable_Energy_Production_Forecaster

we are building a forecaster for renewable energy production, specifically focusing on solar energy. The goal is to predict the amount of energy produced by solar panels based on various features such as weather conditions, time of day, and historical production data.

#  Solar Generation Forecaster

An LSTM-based deep learning system that predicts **next-day solar power generation** for a solar plant using historical weather and generation data.

##  Problem Statement

Small solar plant owners in India must commit to a fixed energy delivery **24 hours in advance**. If they promise 100 units but generate only 20 due to unexpected weather, they face **heavy financial penalties**. This project solves that problem by forecasting tomorrow's generation with high accuracy, allowing owners to make informed commitments.

##  Results

| Metric | Value |
| :--- | :--- |
| **R² Score** | **0.9322** |
| **MAE** | 7.45 kW |
| **RMSE** | 12.20 kW |
| **Training Data** | 5,000 hourly records |
| **Forecast Horizon** | 24 hours |


##  Model Architecture

- **Input:** 24 hours of past weather + generation (7 features)
- **LSTM:** 1 layer, 32 hidden units, dropout=0.3
- **Output:** Next-hour power generation (kW)
- **Training:** 30 epochs, Adam (lr=0.001), MSELoss

##  Features Used

| Feature | Type | Description |
| :--- | :--- | :--- |
| `solar_irradiance_wm2` | Weather | Solar radiation |
| `ambient_temperature_c` | Weather | Air temperature |
| `panel_temperature_c` | Weather | Panel surface temperature |
| `cloud_cover_percent` | Weather | Cloud coverage |
| `hour` | Time | Hour of day (0-23) |
| `day_of_week` | Time | Day of week (0-6) |
| `month` | Time | Month (1-12) |
| `year` | Time | Year |


