# AquaSafe Durban

AquaSafe Durban is a Streamlit data application for exploring documented eThekwini water-service events, historical community risk patterns and short-term system forecasts.

## What the project demonstrates

- Data cleaning and transformation with Pandas
- Community-level historical risk scoring
- Interactive filtering and visualisation
- eThekwini suburb mapping through the municipal GIS service
- Model comparison across Linear Regression, Decision Tree and Random Forest
- Random Forest forecasts for short horizons and a 12-week view
- Clear separation between historical observations and model-generated forecasts

## Data

The repository includes event-level records derived from cited eThekwini Municipality public notices together with prepared analytical datasets used by the dashboard.

Key files:

- `eThekwini_Official_Water_Events.csv` — documented event records
- `Community_Risk_Snapshot.csv` — community-level historical risk features
- `AquaSafe_Weekly_System_Series.csv` — weekly system activity
- `AquaSafe_3_Model_Leaderboard.csv` — validation metrics for compared models
- `AquaSafe_RF_Forecast_7_14_30_Days.csv` — short-horizon forecast summary
- `AquaSafe_RF_12_Week_Forecast.csv` — 12-week Random Forest forecast

## Run locally

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate

pip install -r requirements.txt
streamlit run app.py
```

## Important interpretation note

AquaSafe is an analytical project. Forecasts are model estimates based on the available dataset and should not be interpreted as official municipal service notices or guarantees.

## Tech stack

Python · Streamlit · Pandas · NumPy · Plotly · PyDeck · scikit-learn · eThekwini GIS

## Repository structure

The dashboard is in `app.py`; the model-development workflow is documented in `AquaSafe_Machine_Learning_Model.ipynb`.

## Author

Xolo Dlamini — https://github.com/Itx108
