Sales Forecasting using Machine Learning (Walmart Retail Data)
End-to-end time-series prediction using feature engineering + ML models

Key results
XGBoost
MAE 36897.5222724359
RMSE 52839.25824265576
R2 0.9902509697368989

Built a time-series forecasting pipeline to predict weekly retail sales. Engineered lag and rolling features to capture temporal trends. 
Compared Linear Regression, Random Forest, and XGBoost models. XGBoost achieved the best performance.

Tech stack
Python, Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib

Features
Lag features (Sales_Lag_1, Sales_Lag_4)
Rolling averages and std deviation
Time-based features (month, season, week)
Chronological train-test split
