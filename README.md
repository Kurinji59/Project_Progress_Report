This repository contains the code and analysis used for detecting satellite orbital manoeuvres using XGBoost-based residual anomaly detection. Each notebook corresponds to a specific part of the project:

**EDA.ipynb**
Performs exploratory data analysis on orbital elements (e.g., Brouwer Mean Motion) across multiple satellites. Identifies trends, anomalies, and justifies the choice of BMM for modelling.

**Fengyun_2d.ipynb**
Anomaly detection pipeline for Fengyun-2D. Includes preprocessing, lag feature generation, XGBoost forecasting, residual analysis, and comparison with ground truth manoeuvres.

**Fengyun2E_model.ipynb**
Similar structure to Fengyun-2D, but includes one manually interpolated outlier. Uses a stricter threshold (2 standard deviations) to capture subtle manoeuvres.

**Fengyun2H_model.ipynb**
Applies the same modelling pipeline to Fengyun-2H. No manual outlier removal, threshold set at ±3 standard deviations.

**Jason_3_model.ipynb**
Targets Jason-3, a satellite with flatter BMM trends. Evaluates model performance in low-variance conditions and discusses challenges in detecting manoeuvres.

**sentinel_3a_model.ipynb**
Modelling for Sentinel-3A, which showed clear manoeuvre signals. Demonstrates high alignment between detected anomalies and ground truth using a 3-sigma threshold.
