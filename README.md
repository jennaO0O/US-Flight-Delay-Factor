# 🛫 US Flight Delay Factors

This project investigates the operational and environmental factors contributing to U.S. domestic flight delays. By integrating flight and weather databases, the study employs machine learning to predict delay times and uses scenario-based simulations to quantify the impact of specific delay causes.

---

## 🛠️ Methodology

### Data Integration

* 
**Flight Data (2018–2023)**: Includes airline information, airport locations, and categorized delay types such as NAS, security, and late aircraft.


* 
**Weather Data (2016–2022)**: Covers weather events, severity, and precipitation across 49 states.


* 
**Preprocessing**: The team utilized one-hot encoding for temporal features and handled multicollinearity by dropping baseline categories. Categorical variables were transformed into numerical labels, and missing values were replaced with 0.



### Machine Learning Models

Three models were evaluated using **Root Mean Square Error (RMSE)** as the primary metric:

1. 
**Classification and Regression Tree (CART)**: The best-performing model with an RMSE of **11.6922** and a Mean Absolute Error (MAE) of **3.87 minutes**.


2. 
**Random Forest (RF)**: Achieved an RMSE of **14.6054**.


3. 
**Linear Regression (Lasso)**: Achieved an RMSE of **20.1757**.



---

## 📊 Key Results & "What-If" Simulations

The project used "What-if" simulations to measure how the presence (1) or absence (0) of specific factors changed the predicted mean delay.

### 1. Operational Delay Factors

National Air System (NAS) disruptions—such as heavy air traffic and air traffic control changes—were identified as the most significant predictor of increased delay times.

| Delay Cause | Impact when Present (Min) | Impact when Absent (Min) |
| --- | --- | --- |
| **NAS (National Air System)** | **9.09** | **2.92** |
| **Security** | 7.49 | 5.70 |
| **Late Aircraft** | 6.15 | 5.80 |
| **Carrier** | 5.63 | 6.02 |
| **Weather** | 6.03 | 5.75 |
 

### 2. Weather Event Impacts

Severe weather events exhibited the strongest influence on the model’s predictions, with storms and snow being the primary drivers.

| Weather Event | Impact when Present (Min) | Impact when Absent (Min) |
| --- | --- | --- |
| **Storm** | **13.20** | 12.26 |
| **Snow** | 12.19 | 0.20 |
| **Rain** | 11.29 | 6.01 |
| **Precipitation** | 10.29 | 4.27 |


