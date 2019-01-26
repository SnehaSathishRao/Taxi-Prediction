# Taxi-Prediction
# Business problem:<br/>
Given pickup and dropoff locations, the pickup timestamp, and the passenger count, the objective is to predict the fare of the taxi ride<br/>
# Data:<br/>
Ge the data from : http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml The data used in the attached datasets were collected and provided to the NYC Taxi and Limousine Commission (TLC)<br/>
# Objectives & Constraints:<br/>
**Objectives:** <br/>
Predict number of pick ups as accurately as possible within 10 minutes in a region. <br/>
**Constraints:**<br/>
1. Latency : A medium latency rate is required since the cab driver expect to find pick ups within 10 minutes. <br/>
2. Interpretability : As long as the output doesnt seem mean,the cab driver is not into the interpretation of the result. <br/><br/>
3. Relative Error : Let say the predicted pickups for a particular location are 100, but in actual pickups are 102 the percentage error will be 2% and Absolute error is 2. The taxi driver into percentage error than the absolute error. Let say in some region the predicted pickups are 250, and if taxi driver knows that the relative error is 10% then predicted result will be considered in the range of 225 to 275 which is considerable<br/>
# Machine Learning Problem :<br/><br/>
As mentioned our goal is to predict the fare of taxi ride.Two important preprocessing tasks are involved:<br/>
1. Binning data into 10 mins interval(Since the average time taken to travel 1 mile is 10 minutes in any of the region) <br/>
2. Break NYC into clusters(regions) It is a Time-Series forecasting and regression problem.<br/>
# Performance metrics :<br/>
1. Mean Absolute percentage error(MAPE). 2. Mean Squared error(MSE).<br/>
# Model Summary:

|       Model       |   Train error   |   Test error   |
|--|--|--|
| Linear Regression |  0.113648123791 | 0.129361804204 |
|   Random Forest   | 0.0717619563182 | 0.124542461769 |
|      XGBoost      |  0.119387790351 | 0.115742475694 |
