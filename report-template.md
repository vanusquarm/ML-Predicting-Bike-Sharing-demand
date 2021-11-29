# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Sylvanus Quarm

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
TODO: Add your explanation
Data contained negative values

### What was the top ranked model that performed? 
TODO: Add your explanation
WeightedEnsemble_L3 with score_val of -115.176698 Since the metric for our evaluation is a root_mean_squared,
the model producing the least deviation (or residual) performs best and ranked 1st.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
TODO: Add your explanation
The features season and weather were treated as int. There were resolved by changing the dtype to category
Performing a feature extraction on the datetime feature to obtain an hourly timestamp of the dateset.
This is very important because the total hours used per person to get to his destination affects the counts of rides 

### How much better did your model preform after adding additional features and why do you think that is?
TODO: Add your explanation
Our top model now performs better with score_val of -36.568700 Similarly, all models showed a significant improvement.
There was a 400% improvement in performance. Implying that the hour feature has a correlation with the count of bicycle shares (rides)

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
TODO: Add your explanation
After tuning the model with the GBM and NN options hyperparameter, the training was shorter and an improvement of -36.766750 was achieved

### If you were given more time with this dataset, where do you think you would spend more time?
TODO: Add your explanation
I will spend more time tuning the model with different combinations of hyperparameter options and values

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|default |	default |	default |	1.39622
|add_features|GBM |	NN |	XGB |	0.48147
|hpo|NN |	FASTAI |	GBM |	0.55082

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](img/model_test_score.png)

## Summary
TODO: Add your explanation
Addition of more appropriate features better enhances the model's performance than hyperparameter tuning. Hence, to improve upon your model's performance, identify new features and test its correlation with the target feature (using df.corr()) before fitting it into the model training.