# ⚡ Smart Grid — India Energy Consumption Forecasting

A machine learning project that forecasts India's national electricity demand using POSOCO grid data, with an interactive Streamlit dashboard for exploration and visualization.

---

## 🔍 Project Overview

India's power grid serves 1.4 billion people. Accurate demand forecasting helps grid operators plan capacity, reduce outages, and integrate renewable energy efficiently.

This project:
- Cleans and analyzes 10+ years of POSOCO daily grid data
- Builds an AutoML pipeline to compare multiple forecasting models
- Deploys a **LightGBM model** achieving **1.15% MAPE**
- Visualizes demand trends, renewable growth, and 90-day forecasts in a Streamlit app

---

## 📊 Dashboard Pages

| Page | What it shows |
|------|--------------|
| Overview | National demand KPIs, full historical trend |
| Demand Patterns | Monthly seasonality, weekday vs weekend, year-on-year |
| Renewables | Solar, wind, hydro growth and generation mix |
| Forecast | 90-day ahead prediction with ±5% uncertainty band |
| Model | Actual vs predicted, AutoML model comparison table |

---

## 🧠 Model Performance

| Metric | Value |
|--------|-------|
| Algorithm | LightGBM (AutoML winner) |
| MAPE | **1.15%** |
| R² Score | **0.97+** |
| Test Split | 20% held-out data |

---

## 🗂️ Project Structure

```
smart-grid-india/
├── data/
│   ├── raw/               # CEA and POSOCO source data
│   └── processed/         # Cleaned CSVs
├── notebooks/
│   ├── 01_data_loading.ipynb
│   ├── 02_eda.ipynb
│   ├── 03_preprocessing.ipynb
│   ├── 04_modeling.ipynb
│   └── 05_forecasting.ipynb
├── exports/               # Charts, forecast CSVs, model file
├── app.py                 # Streamlit dashboard
└── requirements.txt
```

---

## 🚀 Run Locally

```bash
# 1. Clone the repo
git clone https://github.com/vedikawaghmare/Smart-Grid-Energy-Consumption-Forecasting.git
cd Smart-Grid-Energy-Consumption-Forecasting

# 2. Install dependencies
pip install -r requirements.txt

# 3. Launch the dashboard
streamlit run app.py
```

---

## 🛠️ Tech Stack

- **Python** — Pandas, NumPy, Scikit-learn, XGBoost, LightGBM
- **Visualization** — Matplotlib, Seaborn
- **Dashboard** — Streamlit
- **AutoML** — PyCaret
- **Data Sources** — POSOCO (Power System Operation Corporation), CEA (Central Electricity Authority)

---

## 📈 Key Insights

- India's grid demand has grown steadily year-on-year, with a visible COVID dip in 2020 and strong recovery
- Peak demand falls in **May–June** driven by summer cooling loads
- Weekday demand runs ~higher than weekends — a reliable pattern for forecasting
- **Solar generation has gone near-vertical since 2020**, outpacing a decade of prior growth

---

## 👩‍💻 Author

**Vedika Waghmare**  
[GitHub](https://github.com/vedikawaghmare) · [LinkedIn](https://linkedin.com/in/vedikawaghmare)
