# Store Item Demand Forecasting

End-to-end retail demand forecasting pipeline using LightGBM, achieving
a volume-weighted MAPE of 7.69% across 2,500 store-item combinations
(50 stores × 50 items) over a 5-year period (2019–2023).

## Results

| Metric | Value | Interpretation |
|--------|-------|----------------|
| MAE    | 2.486 units | Average error per store-item per day |
| wMAPE  | 7.69% | Excellent — below 10% industry benchmark |
| MASE   | 0.466 | 2× more accurate than naive seasonal baseline |

## Project Notebook

All analysis is contained in a single Jupyter notebook covering:

1. **Exploratory Data Analysis** — Sales trends, seasonality patterns,
   promotion effects, price analysis and feature correlations
2. **Feature Engineering** — 40+ features across lag, rolling window,
   calendar, price, promotion, aggregate and interaction categories
3. **Model Training & Evaluation** — Global LightGBM with time-based
   validation, early stopping, and full metric suite including
   MAE, RMSE, MAPE, wMAPE and MASE
4. **Forecasting** — 90-day recursive forecast for all 2,500
   store-item combinations

## Dataset

Synthetic daily retail sales data available on Kaggle — 50 stores × 
50 items × 5 years. Features include sales, price, promotion flag, 
weekday and month.

> Note: Output CSV files and trained model are not included in this
> repository due to file size. Re-run the notebook sequentially to
> reproduce all results.

## Tech Stack

Python · LightGBM · pandas · NumPy · scikit-learn · 
Matplotlib · Seaborn 
