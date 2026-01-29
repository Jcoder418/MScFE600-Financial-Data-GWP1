# MScFE 600 — Financial Data (Group Work Project #1)

## Concise Summary
This Jupyter notebook demonstrates machine-learning-based directional forecasting for ETFs using technical indicators. It covers data preparation, feature engineering (216 technical indicators via Pandas‑TA), feature selection, a neural-network classifier, and evaluation of directional accuracy (up/down predictions).

## Table of contents
- Concise Summary
- Installation & Requirements
- How to run
- Dataset sources
- Methodology & Key Findings
- Tools
- License
- Acknowledgements

## Installation & Requirements
Recommended Python (3.9+). Create and activate a virtual environment, then install required packages:

```bash
python -m venv .venv
source .venv/bin/activate   # or .venv\\Scripts\\activate on Windows
pip install -U pip
pip install pandas numpy scikit-learn pandas-ta yfinance matplotlib plotly tensorflow
```

If you prefer a `requirements.txt`, generate one from your environment or run `pip install -r requirements.txt` if provided.

## How to run
1. Open the notebook `MScFE600-Financial-Data-GWP1.ipynb` in Jupyter or VS Code.
2. Run cells sequentially from top to bottom to reproduce preprocessing, feature computation, model training, and evaluations.
3. To re-download data, run the data-loading cells (they use Yahoo Finance via `yfinance`).

## Dataset sources
- Primary: Yahoo Finance historical daily OHLCV for the ETFs studied (tickers used in the notebook include `ECH`, `EWZ`, and `IVV`).
- The notebook computes technical indicators from OHLCV using `pandas-ta` (about 210 additional indicators).

If you need to fetch the same data programmatically, the notebook includes example code using `yfinance`.

## Methodology & Key Findings
- Feature engineering: 216 features per instrument (OHLCV + technical indicators).
- Preprocessing: rows with NA from rolling computations are dropped and features are min–max scaled to [0,1].
- Target: binary classification of next-day open price movement (up/down).
- Key finding reported in the notebook: selecting ≈5% of features can retain or improve accuracy while reducing model complexity and training time; classification accuracy typically reported near 78–80% on the datasets analyzed.

## Tools
- Python libraries: `pandas`, `numpy`, `pandas-ta`, `scikit-learn`, `tensorflow`/`keras`, `matplotlib`, `plotly`, `yfinance`.

## License
This repository is provided for educational use. Unless you specify otherwise, apply the MIT License (or tell me if you prefer a different license) — add a `LICENSE` file if needed.

## Acknowledgements
- MScFE 600 course materials and project guidelines
- The `pandas-ta` project for technical indicators
- `yfinance` for Yahoo Finance data access

---
If you want additional sections (badges, experiment results summary, or a `requirements.txt`/`LICENSE` file added), tell me and I will add them.
