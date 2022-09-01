# Sale Price per unit of area for Taiwanese homes
**Author:  Blake Shull**
### Final Mode:

My final model is a tuned Bagging Regressor, I checked random forests and a decision tree and tuned all three models.  
I found that tuning the max samples and number of estimators was most helpful for my Bagging Regressor.

### Data:
This Data was found on the UCI.  It is the market historical data set of real estate valuation are collected from Sindian Dist., New Taipei City, Taiwan.

### Model Metrics:

I used Mean Average Error, Mean Squared Error, and Root Mean Squared Error to judge my models.

Mean Average Error - simply the average difference between what the model predicted and what the result was.  This metric, while not useless, can be misleading, seeing as negative and positive errors cancel each other out.

Mean Squared Error - This is the error squared.  While it does not have the problem of negatives and positives cancelling out.  However, it is hard to read.  

Root of Mean Squared Error - This is the best metric to use, seeing as the numbers are brought back down from their misleadingly high squared value in MSE.  However, it still avoids cancelling out like MAE does.

R2 - R2 is the measure of how much of any data point can be explained by our model?  Roughly 3/4 of any data point can be explained, and the remaining 1/4 is unpredictable, or from patterns and variables not available.

The Bagging Regressor was marginally better than all other tuned models, and using PCA on the bagging regressor slightly reduced accuracy and increased variance.  PCA is a process that removes certain variables from the calculation to speed up processing and reduce noise.  In this case, it reduced how much our prediction varied from the actual outcome it was tested against.

Test Scores: 
MAE: 4.24 
MSE: 41.26 
RMSE: 6.42 
R2: 0.74

### Model Uses

I hope the model becomes more useful once I adjust the time, because as is, it is marginally useful.  Longitude, latitude, number of convenience stores near the home, and distance to nearest MRT station are all decent predictors.
Even still, here are the model metrics on the test data:

I would like a higher R2 value, at least in the 80s, and slightly lower variance.  This model has some predictive power for helping us understand how external factors will affect a property value.
I would use it to look for undervalued pieces of property to function as good investments, or purchase homes where conveniences stores are going to be built, for example.

### Methods
I checked the data for duplicates and empty values, but ran into no problems.

Several graphs have been constructed to explore the data, separating out the values that have the most correlation.

The line shows a general pattern associating Mass Rapid Transit stations with price.  As we can see, the line shows a pattern of further homes being of greater value, up to a point, then after that point all homes are roughly equal per unit of area.
![image](https://user-images.githubusercontent.com/107661416/187835350-80a99424-d8ea-4861-8330-bfe4383ebcb7.png)

This bar graph shows a rough positive correlation between proximity of convenience stores and value of home as well.
![image](https://user-images.githubusercontent.com/107661416/187835423-4611d500-e381-410d-8b04-1caee37ee07b.png)

This box plot is useful to visualize which months have what values of homes sold.  While there aren't any particularly strong patterns, it is useful to be able to see slight variations.
![image](https://user-images.githubusercontent.com/107661416/187835447-ac6d26f7-25f0-416d-baf3-9133cf7e48b4.png)



Linear, Decision Tree, and Bagged Tree regressions have all been performed.  These models are all machine learning models that will use the data available to predict our target, home value.  As discussed in the metrics area, bagged regression was slightly the most useful model.  These were done in order to create models that can predict sales.  

### Results

I am moderately happy with the results of this model, but the main problem is that my R2 value is simply too low for my taste.  I would like my model to be able to explain more variance.  

### Recommendations:
For anyone looking to invest in property in New Taipei City, focus on being far from a mass rapid transit station, and near multiple convenience stores.  Additionally, our longitude and latitude findings indicate the Northeast area of the city is the most valuable.

### Limitations & Next Steps
There are three major limitations: first, this is price per area.  The actual home size is not a factor in this data, which would probably be very helpful.  Second, this data set is limited to one city, New Taipei City, in one country in Taiwan in the early 2010s.  Third, the R2 is passable, but more data collection would be very useful.

For further information
For any additional questions, please contact email: blake.shull@gmail.com
