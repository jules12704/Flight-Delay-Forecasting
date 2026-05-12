# Flight Delay Forecasting

Time series forecasting project using 3M US domestic flight records (2019–2023).
Predicts monthly average arrival delays using SARIMA(1,1,1)(1,0,1,12).

## What's in this project
- Full data cleaning pipeline (3M rows → 17 clean columns)
- Exploratory data analysis: time series, airline comparison, heatmap, seasonal decomposition
- Stationarity testing with ADF and KPSS tests
- Model progression: ARIMA(1,2,1) → ARIMA(1,1,1) → SARIMA(1,1,1)(1,0,1,12)
- Benchmarked against seasonal naive baseline and Facebook Prophet (default and tuned)

## Results
| Model | MAE |
|---|---|
| Seasonal Naive | 2.96 min |
| **SARIMA(1,1,1)(1,0,1,12)** | **3.59 min** |
| ARIMA(1,1,1) | 3.89 min |
| Prophet (default) | 4.28 min |
| Prophet (tuned) | 4.54 min |

## Dataset
Kaggle — [US Flight Delay & Cancellation Data (2019–2023)](https://www.kaggle.com/datasets/patrickzel/flight-delay-and-cancellation-dataset-2019-2023)
