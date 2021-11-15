# LSTM for NOx Time Series Prediction

Project for Stockholm Environment Institute.

Supervisor: Xiaoliang Ma, KTH Royal Institute of Technology


## Task
Developing and training LSTM model to predict the hourly NOx concentration data in Stockholm for next 3 days and evaluate the accuracy.

**Univariate Model**

The input only contains NOx concentration. 

**Multivariate model**
Except the NOx data, 

For evaluation, each group must create a **confusion matrix** to capture correct and incorrect classifications. The confusion matrix should be used to quantify the performance of the model using appropriate metrics.

## Methodology & Procedure

### Feature Extraction

#### Spectral Features

| Features       | Notes | Code Link? |
| -------------- | ----- | ---------- |
| R,G,B,NIR |   Raw Intensities    |            |
|       CI1, CI2         |   Cloud    |            |
|     MSVI, VARI, NDVI           |   Vegetation    |            |

#### Texture Features

| Features | Notes | Code Link? |
| -------- | ----- | ---------- |
|   LBP       |       |            |
|   GLCM       |       |            |


#### About Background & No Data

Mask out no data

### Classifier
- Random Prediction
- Naive Bayes
- Logistic Regression
- Linear SVM
- XGBoost

### Evaluation Metrics

- Confusion Matrices
- f1
- recall
- precision


### Training
- First 60 images as train, last 4 images as validation

### Results analysis
- EDA
- Feature Selection
- Plot metrics
- Plot confusion matrix
- Visualize prediction
