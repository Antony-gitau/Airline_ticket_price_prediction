# Airline_ticket_price_prediction

---
## Business problem 
What factors affect the price of airline tickets?

## Dataset
  Understanding data include (but not limited to);
  
  Checking missing values
  
  Checking the data types of the data
  
  Checking the shape of the dataset-  `(10683, 11)` 
  
  Features of the dataset: `'Airline', 'Date_of_Journey', 'Source', 'Destination', 'Route',
       'Dep_Time', 'Arrival_Time', 'Duration', 'Total_Stops',
       'Additional_Info', 'Price'`
   

## Feature encoding
Used one-hot encoding technique. Because this data has no hierachy 

## Outlier detection
Using seaborns boxplot and distplot functions.

## Feature selection
using `mutual_info_classif` class in scikit learn 

## Apply various ML algorithmns
|Algorithmn|training score|r2 score|MSE|MAE|RMSE|
|:--------:|:------------:|:------:|:-:|:-:|:--:|
|RandomForestRegressor|0.9532330591083561|0.8188241648606751|3271201.7583914325|1129.4493479721677|1808.6463884329166|
|LinearRegression|0.6186691314891613|0.602706267686143|7173296.343541427|1929.3244532095798| 2678.3010180973733|
|KNeighborsRegressor|0.784715140845405|0.6162790635344825|6928234.116499766|1732.4331305568555|2632.1538930122924|
|DecisionTreeClassifier|0.8803978935049737|0.646395364855782|6384472.318671034|1407.3724847917642|2526.751336928712|
|DecisionTreeRegressor|0.9666365249758673|0.7393037225262551|4706974.97059923|1246.5433473717046|2169.5563994971944|

## Dumping the model
Using import pickle module -pickle.dump(model)

## Hypertuning.
Using randomizedsearchCV and Gridsearch techniques.

After hypertuning, The `RandomForestRegressor` algorithmn improved to `0.84703670178341` r2 score.

       

