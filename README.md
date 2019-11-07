# Electricity consumption in buildings prediction using RNN

**Source**: [ASHRAE Kaggle competition](https://www.kaggle.com/c/ashrae-energy-prediction/overview). I use a subset of buildings and timestamps, and limit the data to electricity only.<br><br>
**Data (subset)**: <br>
- time-series of electricity consumption (kWh) in different kinds of buildings (hospitals, residential, industrial, etc.). <br>
- Hourly measurements (noisy!!) lasting for about 4 months.<br><br>

**Problem**: create an RNN model that can predict building's electricity consumption in the next 10 hours<br><br>
**Models used**:<br>
1. RNN with 2 LSTM layers and lagged-time-series feature only (test MSE: 0.1396)<br>
2. 3 LSTM layers + lagged-time-series (MSE: 0.1176)<br>
3. 3 LSTM layers + lagged t-s + time features (week, day, hour...) (MSE: 0.1059)<br>
4. Previous model + L2 regularization (MSE: 0.1143)<br>
5. 3 LSTM layers + all features + time-series deltas (MSE: 0.0767)<br><br>

**Example prediction**: <br>Normalized electricity consumption of a building and Model 4 predicted values.<br>![alt text](https://i.ibb.co/Yf2fzk1/download.png)
