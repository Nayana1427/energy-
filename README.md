EV Charging Load Forecasting

A simple and practical machine-learning project that predicts future EV charging energy demand using cleaned historical data and a trained model.

⭐ Features

✨ Predict future EV charging load
📈 Visualize actual vs predicted results
🔮 Generate next-24-hour forecast
🧠 ML model trained using XGBoost
📂 Clean project structure
📊 Rolling and lag-based feature engineering
💾 Model and scaler saved for reuse
🖥 Command-line scripts for training & forecasting
🌐 Optional Streamlit web app

📚 What This Project Does

This project uses historical EV charging data to forecast upcoming energy demand.
It includes everything needed to:

Preprocess and transform raw data

Train a machine learning model

Save the model and scaler

Predict future data

Generate visual charts

Run a user-friendly prediction interface

🚀 Usage
Training the Model

Runs preprocessing + feature engineering + model training.

cd src
python train_and_save.py


This will generate:

models/ev_model.pkl

models/scaler.pkl

Forecasting Future Demand

Predicts the next 24 hours automatically:

python forecast_script.py


This outputs:

models/next_24h_forecast.csv

Viewing Predictions (Graphs)
python visualize.py


Generates:

actual_vs_predicted.png

next_24h_forecast.png

Predicting Custom Values

Use the built-in Streamlit UI:

streamlit run app_streamlit.py


Here you can:

Enter hour, lag features, weekday, etc.

Get predicted EV load instantly

🏷 Data Requirements

Your dataset must include:

timestamp — date/time column

energy_demand — target column

Optional helpful data:

temperature

charger count

station location

usage patterns

The scripts will automatically extract:

hour

day

month

weekday

lag features

rolling averages

🔍 Search / Filtering (Feature Engineering)

The model can use engineered features such as:

demand_lag_1 (previous hour)

demand_lag_24 (same hour previous day)

demand_roll_24_mean

These help the model understand trends and seasonality.

💾 Storage & Persistence

The project stores:

trained model (ev_model.pkl)

scaler (scaler.pkl)

forecasts (next_24h_forecast.csv)

All of these are placed in the /models/ folder.

📱 Compatibility

Works on any system with:

Python 3.8+

pandas, numpy

scikit-learn

xgboost

joblib

matplotlib

streamlit (optional UI)

Install everything using:

pip install -r requirements.txt

🎨 Customization

You can easily customize this project by:

Editing feature engineering in data_preprocessing.py

Adding weather or external APIs

Replacing XGBoost with LSTM or Prophet

Changing look & UI in the Streamlit app

Adding dashboards or cloud deployment

📂 Folder Structure
EV-Charging-Forecasting/
│── data/
│── models/
│── src/
│   ├── data_preprocessing.py
│   ├── train_and_save.py
│   ├── forecast_script.py
│   ├── visualize.py
│   └── app_streamlit.py
│── README.md
│── requirements.txt
