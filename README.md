# Anomaly Detection in Univariate Time Series

My undergraduate thesis at the National Technical University of Athens (NTUA), where I implemented 
and compared a range of anomaly detection algorithms on real-world time series data.

I chose this topic because it sits at the intersection of statistics and machine learning — two areas 
I genuinely enjoy — and has practical applications across many fields, from infrastructure monitoring 
to financial systems.

---

## What this covers

The goal was to benchmark algorithms across different anomaly types (point, collective, contextual, 
and change-point shifts), rather than just picking one method and calling it a day.

The methods are grouped into three categories:

- **Statistical:** SARIMA, Holt-Winters Exponential Smoothing, Linear Models
- **Machine Learning:** Isolation Forest, LOF, OC-SVM, DBSCAN, Matrix Profile, XGBoost
- **Deep Learning:** MLP, LSTM, Autoencoders

---

## Datasets

- **Yahoo Webscope S5 (A1 Benchmark)** — stationary and non-stationary series with various anomaly types
- **NAB NYC Taxi** — taxi demand in New York City, with complex seasonality and window-based anomalies

---

## Methodology

- Data preprocessing: standardization, normalization, linear detrending
- Temporal feature engineering to improve non-sequential ML models
- Hyperparameter tuning via Time Series Cross-Validation and Grid Search
- Comparison of static vs. dynamic thresholding strategies

---

## Key Findings

- **No "one-size-fits-all"** algorithm — performance is highly dependent on the nature of the anomalies
- **Simplicity wins** for point anomalies: Holt-Winters and Isolation Forest proved exceptionally stable
- **Dynamic thresholds** and temporal feature engineering were essential for detecting mean-shift anomalies
- **Deep learning** (Autoencoders, LSTMs) showed competitive advantages in complex, adaptive scenarios
- **NAB Score** evaluation highlighted the importance of timing and precision over mere anomaly coverage

---

## Tech Stack

| Category | Libraries |
|---|---|
| **Language** | [Python](https://www.python.org/) |
| **Core** | [NumPy](https://numpy.org/) · [Pandas](https://pandas.pydata.org/) |
| **ML / DL** | [Scikit-learn](https://scikit-learn.org/) · [TensorFlow/Keras](https://www.tensorflow.org/) · [XGBoost](https://xgboost.readthedocs.io/) |
| **Time Series** | [StatsModels](https://www.statsmodels.org/) · [Stumpy](https://stumpy.readthedocs.io/) |
| **Visualization** | [Matplotlib](https://matplotlib.org/) · [Seaborn](https://seaborn.pydata.org/) |
