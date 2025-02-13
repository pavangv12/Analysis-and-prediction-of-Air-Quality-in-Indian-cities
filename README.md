# Air Quality Analysis and Prediction in Indian Cities

## Overview
Air pollution is a growing crisis in India, affecting public health and the economy. This project aims to analyze air pollution levels across six major Indian cities: Bengaluru, Chennai, Delhi, Hyderabad, Kolkata, and Mumbai. The dataset includes hourly air quality measurements from 2019 to 2023, enabling us to study pollutant trends, seasonal variations, and their impact on the Air Quality Index (AQI).

## Problem Statement
All of India’s 1.4 billion people are exposed to unhealthy levels of harmful pollutants from multiple sources. This project aims to:
- Analyze and understand major air pollutants and AQI trends.
- Identify patterns that provide data-backed insights.
- Develop a system to alert citizens about air quality levels and recommend protective measures.

## Dataset Details
**Source:** Central Control Room for Air Quality Management - [CPCB](https://airquality.cpcb.gov.in/ccr/)

**Cities Covered:** Bengaluru, Chennai, Delhi, Hyderabad, Kolkata, Mumbai  

**Time Period:** 2019 - 2023  

**Total Entries:** 262,944  

**Key Attributes:**
- **Timestamp & City:** Location and time of each reading.
- **Pollutants Measured:** PM2.5, PM10, NO, NO2, NOx, NH3, SO2, CO, Ozone, Benzene, Toluene, Xylene, O Xylene, Eth-Benzene, MP-Xylene.
- **Weather Data:** Temperature (AT), Humidity (RH), Wind Speed (WS), Wind Direction (WD), Rainfall (RF & TOT-RF), Solar Radiation (SR), Barometric Pressure (BP), Vertical Wind Speed (VWS).
- **AQI Calculation:** Computed using pollutant levels, categorized based on national standards.

## Project Objectives
### 1. **Data Analysis & Visualization**
- Study pollutant distribution across cities and over time.
- Identify seasonal and yearly AQI trends.
- Analyze environmental factors influencing AQI.
- Compare industrial vs. vehicular pollution levels.

### 2. **Machine Learning Models for Prediction**
- Train models to predict AQI based on pollutant data.
- Forecast AQI for a given city on a future date.
- Fine-tune models using hyperparameter optimization.
- Deploy a real-time AQI prediction system.

## Tech Stack
- **Programming Language:** Python
- **Data Handling & Analysis:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn, Plotly
- **Machine Learning & Modeling:** Scikit-learn, XGBoost, CatBoost, PyTorch (LSTM)
- **Deployment:** Flask, Streamlit, Google Drive for dataset storage

## Model Performance
**Evaluation Metrics:** Root Mean Squared Error (RMSE), Training & Validation Accuracy

| Model | RMSE | Training Accuracy | Testing Accuracy | Validation Accuracy |
|--------|------|------------------|------------------|------------------|
| Linear Regression | 39.07 | 79.8% | 80.5% | 79.5% |
| Decision Tree Regressor | 44.94 | 100% | 67.3% | 72.6% |
| Random Forest (Grid Search) | 31.48 | 98.2% | 83.0% | 86.4% |
| Random Forest (Randomized Search) | 31.38 | 98.2% | 83.0% | 86.4% |
| CatBoost | 32.19 | 87.9% | 83.6% | 86.2% |
| XGBoost | 31.79 | 93.0% | 83.0% | 86.5% |

**Best Model:** Random Forest (Randomized Search) with 86.4% validation accuracy

## Deployment & Future Enhancements
- **Real-Time AQI Dashboard:** Live monitoring & visualization of AQI levels.
- **Predictive Alerts:** Early warnings based on machine learning predictions.
- **Integration with Social Media & Maps:** Awareness campaigns and location-based pollution alerts.

## How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/pavangv12/Analysis-and-prediction-of-Air-Quality-in-Indian-cities.git
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the analysis and model training:
   ```bash
   python train_model.py
   ```
4. Deploy the prediction system:
   ```bash
   streamlit run app.py
   ```


