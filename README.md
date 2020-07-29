# FIFA 20 - Market value prediction

This was my final "Capstone" project at neuefische-Bootcamp in Hamburg in May 2020.

## Main Deliveries:

* **Business presentation** of my whole project. You can find the presentation directly in this repo ("FC_Python_Business_Presentation")
* **Interactive bokeh dashboard**, which displays differences between my model predictions and transfermarkt.de market values as under- and overvaluations by the videogame mFIFA20 (you can read more on this in the following). You can access the dashboard [here](https://fw-capstone-hh-feb2020.herokuapp.com/app).

**Preview of Dashboard**
![](https://github.com/fabwerk90/FIFA-20---Market-value-prediction/blob/master/Dashboard_Preview.PNG)

## Summary:

* In this project I aimed at finding a Machine-Learning model in order to predict market values of football players (sourced from transfermarkt.de) with player attributes and ratings from the video game "FIFA 20". 
* By applying different kinds of regression models I was able to determine the best models for this approach (namely: Random Forest, Gredient Descent Boost and XGBoost).
* In a last step I applied the stacking method in order to find the best predictions possible.
* My aim was to find the overall best predictions, thus the target metrics I was aiming for were MAE, MRSE and R-Squared.


## Structure of the repository:

In this repository you find the whole process of my approach. To maintain a good overview, the notebooks are splitted in the following order:

Contents:
- "1_Data_Work" (includes Data Mining, Data Merging and Data Cleaning)
- "2_first_EDA" (Exploratory Data Analysis ("EDA))
- "3_Feature_Engineering"
- "4_second_EDA" (2nd EDA after feature engineering)
- "5_Predictive_Modeling" (feature and model selection, predictions and stacking)



## Business Case:

### Market values in Football:
* Football players are an investment object in terms of market value, since they can be sold or bought by football clubs. 
* Estimating and predicting these values is of crucial interest for football clubs, in order to evaluate own and potential new players.
* [transfermarkt.de](www.transfermarkt.de) is a database, which provides market value estimations for nearly every player around the world. Transfermarkt uses “crowd estimation”*  to estimate player market values (basically a network of volunteer data reviewers)
* To which degree are player attributes and ratings from the video game “FIFA 20” able to perform these estimations and predictions? EA (publisher of FIFA) estimates player ratings and attributes depending on a network of professional data reviewers.

### Key Takeaways:
* English, Spanish, Italian, German and French first league dominate in terms of market value .
* Market values increase with age up to a peak  performance age and decrease thereafter.
* Market values increase nearly exponentially with FIFA player rating.
* League, age and FIFA rating are also the features with most predictive power.
* Prediction deviations from actual values (from transfermarkt) lie between 123.000 € (for goalkeepers) and 250.000 € (for field players) in the median.

### Big picture:
* I assumed, that transfermarkt.de market values estimates real world market values somewhat realistically.
* If we assume that transfermarkt is a better estimator of real world market values, this would imply, that prediction deviations from actual market values should be treated as over- and under-valuations by the FIFA20 videogame.
* In order to illustrate this, I've build an interactive bokeh dashboard. A link to this dashboard can be found at the beginning of this readme under "Main Delivery".



### Future Work:
* Gather transfermarkt and FIFA data from previous years and lookup how under- and overvalued players developed  in terms of market value.
* Follow up on how under- and overvalued players are developing in terms of market value in the future
* Apply neural networks on the data and see if model predictions improve




