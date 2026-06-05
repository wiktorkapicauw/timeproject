# Forecasting Google Trends with VAR and SARIMA

Monthly Google Trends search-interest series for "natural gas" and "electricity prices" (United Kingdom, 2010-2026) are forecast with a vector autoregression (VAR) and two univariate SARIMA models, and their out-of-sample accuracy is compared. The full analysis - stationarity and Granger-causality testing, model specification and diagnostics, impulse-response and forecast-error-variance decomposition, forecasting and error comparison - is in the notebook.

Notebook: [`notebooks/topic2_var_sarima.ipynb`](notebooks/topic2_var_sarima.ipynb)

## Setup

```bash
python -m venv .venv
# Windows: .venv\Scripts\activate     Linux/macOS: source .venv/bin/activate
pip install -r requirements.txt
jupyter lab notebooks/topic2_var_sarima.ipynb
```

## Data

`data/trends_naturalgas_electricityprices_GB.csv` holds the two series (Google Trends index, 0-100), pulled together so they share a common scale. The notebook reads this CSV by default; set `FETCH = True` in the data-loading cell to re-download it with `pytrends`.
