Corporación Favorita — Retail Demand Forecasting (Streamlit App)

This project predicts daily product sales for Corporación Favorita, a major retail chain in Ecuador.
It deploys the best XGBoost model into a Streamlit web app, enabling interactive forecasting for selected stores and SKUs.

Project Overview

The goal is to forecast sales for January–March 2014 for stores located in the Guayas region.
Demand forecasting helps planners optimize inventory, promotions, and staffing decisions.

This app demonstrates how a trained ML model can be operationalized for business users through an easy-to-use interface.

Model Summary
Feature	Description
Model Type	XGBoost Regressor
Training Data	Daily sales, oil prices, holidays, and promotions
Forecast Horizon	90 days (Jan–Mar 2014)
Metric Used	RMSE (Root Mean Squared Error)
Why XGBoost?	Best validation performance compared to other models (e.g., LSTM, Linear Regression)
App Features

Streamlit Web Interface: Interactive and intuitive forecasting dashboard.

Store & SKU Selection: Choose from available stores and product items.

Forecast Visualization: Historical trends + future predictions in one chart.

Downloadable Results: Export forecasts as CSV files.

Modular Structure: Organized codebase for scalability and maintainability.

Folder Structure
retail_demand_forecast/
│
├── app/
│   ├── main.py          # Streamlit app UI
│   ├── config.py        # Paths, constants, and parameters
│   └── __init__.py
│
├── data/
│   ├── data_utils.py    # Data loading and preprocessing helpers
│   └── __init__.py
│
├── model/
│   ├── model_utils.py   # Model loading and forecasting logic
│   └── __init__.py
│
├── mlflow_results/      # Local MLflow tracking folder
│
├── requirements.txt
└── README.md

How to Run Locally

Clone the repository

git clone https://github.com/Tigi-koko/retail_demand_forecast.git
cd retail_demand_forecast


Install dependencies

pip install -r requirements.txt


Run the Streamlit app

streamlit run app/main.py


Open in your browser

http://localhost:8501

Screenshots

(Add your Streamlit interface screenshots here — e.g., store & SKU selection, forecast plots, etc.)

Notes

Make sure xgb_tuned.pkl, scaler.pkl, and features.txt are available in the model_artifacts/ folder.

If loading artifacts causes an error, retrain or re-save the files using your Week 3 notebook.

Context

Developed for Sprint 4 of the Advanced Data Science Capstone.
Focus: Forecast deployment, business usability, and model operationalization.
