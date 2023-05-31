# Report: Predict Bike Sharing Demand with AutoGluon Solution

#### Qudus Abolade

## Initial Training

### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?

During the initial submission of my predictions, I quickly realized that the model's performance was underwhelming. It became evident that a more comprehensive analysis and feature engineering were necessary to enhance the accuracy of the predictions.

### What was the top ranked model that performed?

Among the models I trained, the one that stood out as the top performer was the impressive WeightedEnsemble_L3. Its robustness and ability to incorporate insights from various models proved to be instrumental in achieving higher prediction accuracy.

## Exploratory data analysis and feature creation

### What did the exploratory analysis find and how did you add additional features?

Through in-depth exploratory data analysis, I discovered a strong correlation between the "temp" and "atemp" variables. Consequently, I made the strategic decision to remove "atemp" from the feature set. Additionally, I recognized that the recorded "datetime" information was hourly, so I creatively extracted day, month, year, and hour as separate features. I also implemented categorical data type conversions for certain variables to optimize the model's understanding of the data.

### How much better did your model preform after adding additional features and why do you think that is?

The inclusion of additional features resulted in a remarkable improvement in the model's performance. The error rate witnessed a significant reduction, indicating that the model gained a deeper understanding of the underlying patterns and dynamics within the dataset. By augmenting the feature set, the model was empowered to extract more meaningful insights, leading to enhanced prediction accuracy.

## Hyper parameter tuning

### How much better did your model preform after trying different hyper parameters?

Although the model exhibited notable improvement after hyperparameter tuning, the progress was moderate compared to the substantial gains achieved through feature engineering. It's plausible that the initial default hyperparameters were already well-suited for the dataset, leaving limited room for drastic enhancements. Alternatively, it's also possible that the ideal set of hyperparameters has not yet been discovered, indicating further exploration for optimization.

### If you were given more time with this dataset, where do you think you would spend more time?

Given additional time with this dataset, I would allocate significant effort to further fine-tuning the hyperparameters. Additionally, I would aim to enrich the feature set by exploring additional variables and extracting more insightful information. Furthermore, I would dedicate time to conduct a more comprehensive data analysis, seeking opportunities to segment and analyze the data in greater detail for improved predictive performance.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score

|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|default_values|default_values|default_values|1.80|
|add_features|default_values|default_values|default_values|0.72|
|hpo|GBM: num_leaves: lower=26, upper=66|XGB: max_depth lower=5, upper=9|refit_full='best'|0.49|

### Create a line plot showing the top model score for the three (or more) training runs during the project

![model_train_score.png](img/modelscore.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project

![model_test_score.png](img/output.png)

## Summary

In summary, for this project, I used all concepts taught in the first lesson. I used AutoGluon to train a model to predict the number of bikes that will be rented in a given hour. I first submitted the project without any analysis or feature engineering. The model performed poorly. I was able to improve the model by adding more features and tuning the hyperparameters. I was able to reduce the error from 1.80 to 0.49.
