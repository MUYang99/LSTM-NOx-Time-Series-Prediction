# LSTM for NOx Time Series Prediction

[Subproject for Stockholm Environmental Institute](https://www.kth.se/profile/liang/page/green-transport-solutions-using-iot-sensors)

Supervisor: [Xiaoliang MA, KTH Royal Institute of Technology](https://www.kth.se/profile/liang)

## Task
Developing and training LSTM model to predict the hourly NOx concentration data in Stockholm for next 3 days and evaluate the accuracy.

## Methodology & Procedure

### Data Inputs

- Inputs of Univariate Model

The inputs only contains NOx concentration. 

- Inputs of Multivariate model

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
Data of 1.1-12.31/2015 as train, 1.1-1.3/2016 as validation

### Evaluation

The prediction and the ground truth of next 3 days are visualized in a figure, and RMSE, MAE, MAPE, MedAE, r2_score and explained_variance_score are used for evaluation
