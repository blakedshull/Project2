# Sale Price per unit of area for Taiwanese homes
**Author:  Blake Shull**
### Final Mode:

My final model is a tuned Bagging Regressor, I checked random forests and a decision tree and tuned all three models.  
I found that tuning the max samples and number of estimators was most helpful for my Bagging Regressor.

### Model Metrics:

I used Mean Average Error, Mean Squared Error, and Root Mean Squared Error to judge my models.  The Bagging Regressor was marginally better than all other tuned models,
and using PCA on the bagging regressor slightly reduced accuracy and increased variance.  
MAE: 2.30 
MSE: 13.17 
RMSE: 3.63 
R2: 0.93

### Model Uses

I hope the model becomes more useful once I adjust the time, because as is, it is marginally useful.  Longitude, latitude, number of convenience stores near the home, and distance to nearest MRT station are all decent predictors.
Even still, here are the model metrics on the test data:
MAE: 4.03 
MSE: 37.77 
RMSE: 6.15 
R2: 0.76

I would like a higher R2 value, at least in the 80s, and slightly lower variance.  This model has some predictive power for helping us understand how external factors will affect a property value.
I would use it to look for undervalued pieces of property to function as good investments, or purchase homes where conveniences stores are going to be built, for example.
