# NYC-TAXI-PROBLEM

# NYC Taxi Trip Duration Prediction 🚖📊

📌 Overview
This project aims to predict the duration of taxi trips in New York City using historical ride data. Leveraging Python and machine learning, the project goes through a full data science pipeline — from raw data cleaning to model deployment insights.

---

🧰 Tools & Libraries Used

- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Scikit-learn, XGBoost


---

 🗃 Dataset
- **Source**: [NYC Taxi Trip Duration | Kaggle](https://www.kaggle.com/c/nyc-taxi-trip-duration)
- Includes ~145k ride entries with pickup/dropoff datetime, coordinates, trip duration, vendor IDs, etc.

---

📊 Key Steps

 1. Exploratory Data Analysis (EDA)

- Distribution of trip duration
- Peak taxi demand hours
- Vendor-wise passenger patterns
- Trip duration variation across days and time slots

 2. Feature Engineering

- `trip_distance` using Haversine formula
- `avg_speed_kmh`
- Rush hour and weekend flags
- Passenger × distance interaction term
- Log-transformed `trip_duration` to handle skewness

 
 3. Outlier Detection

- IQR method
- Log normalization to improve variance stability

 4. Modeling

-  Algorithm used: **XGBoost Regressor**
- Tuned via GridSearchCV

- Evaluation metrics:
  - 📉 **MAE**: ~48 seconds
  - 🧠 **R² Score**: 0.966

- Visual validation with actual vs predicted comparison

---

 
 📈 Findings

- Longer trips naturally align with longer durations (strong distance-duration correlation)
- Weekday trips show more predictable behavior due to structured travel patterns
- Vendor 2 had a higher average passenger count per trip
