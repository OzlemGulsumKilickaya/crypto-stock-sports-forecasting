# 📈 Solana Price Prediction API Project

This repository contains the full pipeline for building, training, and deploying machine learning models to forecast Solana cryptocurrency prices. It includes data ingestion, model training (Linear Regression, Random Forest, XGBoost), serialization, and integration-ready API templates.

---

## 🔍 Overview

- **Asset**: Solana (SOL)
- **Objective**: Predict future Solana prices based on hourly historical data
- **Tech Stack**:
  - Python (data preprocessing & modeling)
  - Jupyter Notebook (development and training)
  - Pickled ML models (`.pkl`) for deployment
  - API templates (FastAPI or Flask-style)

---

## 🧱 Project Structure

solana-price-prediction-api/
├── data/
│ └── solana_hourly.csv # Historical price data
│
├── scripts/
│ └── fetch_solana.py # Solana data collection script
│
├── models/
│ ├── linear_regression_model.pkl
│ ├── random_forest_model.pkl
│ └── xgboost_model.pkl # Serialized trained models
│
├── notebooks/
│ └── notebook_analysis.ipynb # Main modeling & training notebook
│
├── api_templates/
│ └── [FastAPI/Flask-ready code here]
│
├── docs/
│ ├── 4C_Technical_Doc_Crypto_Stocks_Predictions_V1.pdf
│ └── Planning_General.docx
│
├── LICENSE
├── .gitignore
└── README.md


---

## 📊 Modeling Approach

The notebook includes:
- Data import and time-based feature engineering
- Data splitting (train/test)
- Model training:
  - 🔹 **Linear Regression**
  - 🌲 **Random Forest**
  - 🚀 **XGBoost**
- Model evaluation with metrics (MAE, RMSE, R²)
- Export of trained models as `.pkl` for API usage

---

## ⚙️ API Deployment

Model files are ready to be served via API. Example routes:
- `/predict`: POST request with recent time-series input
- `/retrain`: Optional endpoint for model refresh with new data

You can use FastAPI, Flask, or another framework of your choice.

---

## ▶️ How to Run

1. Install dependencies:
   ```bash
   pip install pandas numpy scikit-learn xgboost matplotlib fastapi uvicorn


Launch the notebook:

jupyter notebook notebooks/notebook_analysis.ipynb

Start the API (if using FastAPI):

uvicorn app.main:app --reload

🙌 Acknowledgments
Solana price data from public APIs or third-party aggregators

API and model deployment inspired by common FinTech use cases
