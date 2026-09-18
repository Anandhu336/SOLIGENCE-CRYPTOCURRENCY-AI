# SOLIGENCE Cryptocurrency AI

A Streamlit application for analyzing, forecasting, and tracking cryptocurrencies (LTC-USD, BTC-USD, ETH-USD, BCH-USD). Combines historical data visualization, correlation/clustering analysis, and four forecasting approaches (Random Forest, SARIMAX, LSTM, Prophet), plus a live crypto news feed.

## Features
- Home - welcome screen for the SOLIGENCE trading platform
- Historical Data Viewer - view cleaned historical price data for a chosen cryptocurrency and date range, with moving-average line charts and candlestick charts
- Correlation Analysis - clusters cryptocurrencies, reports a silhouette score, and shows correlation heatmaps (per-cluster and global)
- Data Visualizations - exploratory data analysis: price trends over time, KDE distribution plots, rolling volatility, candlestick charts, seasonal decomposition, and daily returns distribution
- Random Forest Forecasting - predicts market state (e.g. up/down) using a Random Forest classifier, with accuracy score and forecast chart
- SARIMAX Forecasting - time-series forecasting with a SARIMAX model
- LSTM Forecasting - deep learning price forecasting with an LSTM network, including predicted highs/lows
- Prophet Forecasting - forecasting with Facebook Prophet, with a live training progress bar
- Cryptocurrency News - latest crypto news pulled from a news API

## Tech stack
- Python
- Streamlit (UI)
- pandas / numpy
- scikit-learn (Random Forest, clustering)
- statsmodels (SARIMAX)
- TensorFlow / Keras (LSTM)
- Prophet (time-series forecasting)
- Plotly, matplotlib, seaborn (charts and heatmaps)

## Project structure
- `app.ipynb` - main Streamlit app tying all modules together
- `data_fetcher.ipynb` - fetches real-time/historical cryptocurrency data
- `data_prep_cluster.ipynb` - data preparation and clustering
- `correlation_analysis.ipynb` - correlation analysis and clustering used by the Correlation Analysis page
- `crypto_visualizations.ipynb` - EDA plots used by the Data Visualizations page
- `random_forest_crypto.ipynb` - Random Forest forecasting pipeline
- `sarimax_forecasting.ipynb` - SARIMAX forecasting pipeline
- `lstm_forecasting_module.ipynb` - LSTM forecasting pipeline
- `prophet_forecasting_module.ipynb` - Prophet forecasting pipeline
- `crypto_news.ipynb` - fetches the latest cryptocurrency news
- `Applied AI in Business (COM724) AE2 REPORT.pdf` - project write-up/report

## Getting started
```bash
git clone https://github.com/Anandhu336/SOLIGENCE-CRYPTOCURRENCY-AI.git
cd SOLIGENCE-CRYPTOCURRENCY-AI
pip install streamlit pandas numpy scikit-learn statsmodels tensorflow prophet plotly matplotlib seaborn
```
Note: the app's modules (`crypto_visualizations`, `correlation_analysis`, etc.) are Jupyter notebooks, not `.py` files. To run `app.ipynb` as a Streamlit app, export the notebooks to `.py` scripts first (e.g. `jupyter nbconvert --to script *.ipynb`) so they can be imported, then run:
```bash
streamlit run app.py
```

## Usage
1. Launch the app and use the sidebar to navigate between pages.
2. Pick a cryptocurrency (LTC-USD, BTC-USD, ETH-USD, or BCH-USD) on the relevant page.
3. Explore historical data, correlation/clustering results, EDA visualizations, or run one of the four forecasting models to see its accuracy and forecast chart.
4. Check the Cryptocurrency News page for the latest headlines.
