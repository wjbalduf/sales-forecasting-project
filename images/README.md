Feature Engineering

To improve predictive performance, the following features were created:

Time-based features:
Year, Month, Week, Quarter
Day of Week
Season (Winter, Spring, Summer, Fall)
Lag features:
Sales_Lag_1
Sales_Lag_4
Rolling statistics:
4-week rolling mean
12-week rolling mean
4-week rolling standard deviation

These features allow the model to capture temporal dependencies and trends in sales data.

Models Used include:

1. Baseline Model
Simple lag-based forecasting (Sales_Lag_1)
Serves as a benchmark for comparison
2. Linear Regression
Two versions:
Basic (calendar + economic features)
Enhanced (adds lag + rolling features)
3. Random Forest Regressor
Captures nonlinear relationships in the data
Improves performance over linear models
4. XGBoost Regressor (Final Model)
Gradient boosting model
Best overall performance

Model Performance:

1. Basic Linear Regression
MAE 417432.7435536207
RMSE 495604.6968130665
R2 0.1423327619457948
2. Enhanced Linear Regression
MAE 53457.32529535927
RMSE 73172.7030932309
R2 0.981304107972177
3. RANDOM FOREST RESULTS
MAE 42522.134997094
RMSE 61186.08731585186
R2 0.9869276593038431
4. XGBOOST RESULTS
MAE 36897.5222724359
RMSE 52839.25824265576
R2 0.9902509697368989

- Feature engineering had the largest impact on model performance
- Lag and rolling features significantly improved predictive accuracy
- Sales data exhibits strong temporal autocorrelation
- Tree-based models (Random Forest, XGBoost) provided marginal improvements over linear regression
- XGBoost achieved the best overall performance

Final Result:

The best performing model was XGBoost:

MAE 36897.5222724359
RMSE 52839.25824265576
R2 0.9902509697368989

This indicates that the model explains nearly all variance in weekly sales.

Tech Stack:
Python
Pandas / NumPy
Scikit-learn
XGBoost
Matplotlib / Seaborn
Joblib

Business Value

This forecasting system can be used to:
Predict retail demand
Improve inventory planning
Reduce stockouts and overstocking
Support data-driven decision making in retail operations

Future Improvements:
Hyperparameter tuning (GridSearch / Optuna)
Cross-validation with time-series splits
External feature integration (promotions, holidays)
Deep learning models (LSTM / Transformers)

Author

Built as a data science portfolio project focused on time-series forecasting and machine learning pipelines.

Key Takeaway

The majority of predictive power came from engineered lag and rolling features, showing that historical sales patterns are the strongest driver of future demand.