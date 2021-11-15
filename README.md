# LSTM for NOx Time Series Prediction

Supervisor: Xiaoliang Ma, KTH Royal Institute of Technology

## Task
Developing and training LSTM model to predict the hourly NOx concentration data in Stockholm for next 3 days and evaluate the accuracy.

## Methodology & Procedure

### Data Inputs

**Univariate Model Inputs**

The inputs only contains NOx concentration. 

**Multivariate model Inputs**

Except the NOx data, the input also contains environmental data such as Difftemp, Global radiation, STD WD, STD WS, STD VertWind, Temp, WD and WS.

### Data Analysis & Processing

- Time lag acf & pacf, FFT
- Outliers detection: Density curve, Box-plot
- Drop nan
- Data normalization

### Models Construction

#### Univariate Model

| Model       | Notes |
| ------------| ----- |
| LSTM        | Keras |
| Prophet     | fbprophet |
| Xgboost     | xgboost |
| ARIMA     | statsmodels |
| SVM     | sklearn |
| KNN     | sklearn |
| Bayes     | sklearn |
| DecisionTree     | sklearn |

#### Multivariate model

| Features | Notes |
| -------- | ----- | 
|   LSTM       |   Keras    |
| DecisionTree | sklearn |
| Xgboost     | xgboost |


### Training
Data from 2015.1.1 to 2015.12.31 as train, 2016.1.1 to 2016.1.3 as validation

### Evaluation

The prediction and the ground truth of next 3 days are visualized in a figure, and RMSE, MAE, MAPE, MedAE, r2_score and explained_variance_score are used for evaluation
