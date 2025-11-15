
Electric Vehicle Charging Load Forecasting Using ML
This project predicts future EV (Electric Vehicle) charging energy demand using machine learning.
It helps to estimate how much electricity EV chargers will use in the next few hours or days.
This is useful for:

1.Power grid management
2.Charging station planning
3.Reducing overload and blackouts
4.Energy cost optimization

The project uses a cleaned dataset, trains a machine learning model, and forecasts future energy demand.

This project includes:

> Cleaned dataset (cleaned_ev_charging_dataset.csv)
Contains timestamp-based EV charging energy data.

> Preprocessing script
Cleans the data and creates features like hour, weekday, lag values, etc.

> Model training script
Trains an XGBoost model and saves it as ev_model.pkl.

> Scaling tool (scaler.pkl)
The scaler ensures new data matches training format.

> Forecasting script
Predicts the next 24 hours (or custom hours).

> Visualization script
Creates graphs like:
Actual vs Predicted
24-hour forecast graph

> Optional Streamlit App
A simple user interface to view predictions.

Requirements

Install all needed libraries using:

pip install -r requirements.txt


The main libraries used are:

pandas
numpy
scikit-learn
xgboost
matplotlib
joblib

How to Run the Project

1️⃣ Place your dataset

2️⃣ Train the Model

3️⃣ Forecast the Next 24 Hours

4️⃣ Visualize the Results

Goal of This Project

The aim is to build a complete end-to-end EV charging forecasting system, including:
data preprocessing
feature engineering
machine learning
forecasting
visualization





