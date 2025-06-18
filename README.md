# Time Series Forecasting for Desalination Systems

A **novel hybrid time series modeling approach** that combines **SARIMA** and **Support Vector Regression (SVR)** to accurately forecast **membrane performance in desalination systems**. This approach **fuses statistical and machine learning techniques** to effectively model both **seasonal trends and nonlinear disturbances** in membrane flux data (e.g., fouling, wetting).

## Novelty & Contribution

- Introduces a hybrid SARIMA-SVR model to forecast membrane flux in desalination systems.
- Enhances accuracy by capturing both seasonal trends and irregular fluctuations in the data.
- Integrates statistical time-series modeling with machine learning for more robust predictions.
- Enables 48-hour advance detection of membrane fouling and wetting, supporting predictive maintenance.

This hybrid approach supports smart, data-driven predictive maintenance in **Membrane Distillation (MD)** systems.

## Problem Statement

Membrane Distillation (MD) is a promising alternative to reverse osmosis. However, it suffers from:

- **Membrane Fouling** – gradual clogging that reduces water output.
- **Membrane Wetting** – saltwater penetration that contaminates the product.

These issues degrade system performance, increase energy demands, and reduce operational lifespan.

## Solution

A **hybrid time series model** is implemented:

- **SARIMA** models seasonal and long-term trends in flux behavior.
- **SVR** captures residual non-linear dynamics missed by SARIMA.

This dual-layered modeling improves robustness, precision, and enables early detection of performance degradation.

## Files Included

- `water_Flux1.ipynb`: Time series modeling of water flux.
- `Salt_Flux1.ipynb`: Time series modeling of salt flux.

## Methodology Overview

1. **Stationarity Checks & Differencing**
2. **Model Training**  
   - SARIMA applied to the base time series.  
   - SVR trained on SARIMA residuals.  
3. **Forecast Combination** (Hybrid)
4. **Model Evaluation** using RMSE, MAE, NRMSE, MedAE, TIC

## Key Results

| Model        | Salt Flux RMSE | Water Flux RMSE |
|--------------|----------------|------------------|
| SARIMA       | 0.0691         | 0.3985           |
| SVR          | 0.0662         | 0.3689           |
| **Hybrid**   | **0.0596**     | **0.3331**       |

The hybrid model achieved the **lowest error rates**, effectively modeling both structured patterns and anomalies.

## Technologies Used

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- `statsmodels` (SARIMA)
- `scikit-learn` (SVR)
- Jupyter Notebook

## Real-World Impact

- Supports **real-time predictive maintenance** in desalination plants.
- Reduces operational downtime and associated costs.
- Provides a scalable forecasting solution using **existing sensor data**—no additional hardware required.
