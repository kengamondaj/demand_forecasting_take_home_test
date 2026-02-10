# Demand Forecasting (1–28 Days)

This repo contains an end‑to‑end time‑series demand forecasting workflow with rolling time‑series validation, baseline comparisons, and ML models (HistGBR + XGBoost). The notebook is designed for both business and technical review.

## Contents
- `Code.ipynb` – Clean, narrative notebook with EDA, feature engineering, modeling, evaluation, diagnostics, and 28‑day forecasts.
- `demand_forecasting_assignment.csv` – Input dataset.
- `requirements.txt` – Minimal dependencies needed to run the notebook.

## How to Run
1. Create a Python environment (recommended).
2. Install dependencies:
   - `pip install -r requirements.txt`
3. Open `Code.ipynb` and run all cells.

## Notes
- The notebook uses **date‑based 4‑fold time‑series CV** to avoid leakage and ensure all store×SKU pairs appear in train and validation.
- Evaluation includes both standard and **recursive multi‑step** metrics to simulate real 28‑day forecasting.
- WAPE is emphasized due to intermittent demand and zeros.

## Output
- Model comparisons and diagnostics are produced in‑notebook.
- A 28‑day forecast is generated for all store×SKU pairs.

