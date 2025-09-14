
# Stock Price Prediction (Uniqlo / Fast Retailing, 2012–2016)

This project predicts the **next-day closing price** using historical OHLCV data.
It’s a supervised learning **regression** problem built for CSCA 5622.

##  Repo Contents
- `notebook/ML-finalproject.ipynb` — main analysis (EDA, features, models, results)
- `reports/figures/` — plots used in the report
- `src/` — optional helpers (feature engineering, training)
- `requirements.txt` — Python dependencies
- `data/README_DATA.md` — how to obtain the dataset (we don’t commit data)

##  Method
- EDA: trends, returns distribution, correlations
- Features: lagged closes, moving averages, rolling std, volume MAs, spreads
- Models: Linear/Ridge/Lasso, RandomForest, GradientBoosting
- Split: Time-based (Train: 2012–2015, Test: 2016)
- Metrics: RMSE, MAE, R²

##  Quickstart
```bash
# 1) clone
git clone https://github.com/<your-username>/stock-price-prediction-uniqlo.git
cd stock-price-prediction-uniqlo

# 2) create env & install
python -m venv .venv && source .venv/bin/activate   # (Windows: .venv\Scripts\activate)
pip install -r requirements.txt

# 3) get data (see data/README_DATA.md)
#    place CSV at: data/stocks2012-2016.csv

# 4) open the notebook
jupyter notebook notebook/ML-finalproject.ipynb
