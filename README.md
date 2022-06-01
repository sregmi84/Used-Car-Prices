# Used-Car-Prices
Used Kaggle used car data to build model that predicts their price. Models to try to be expanded in the future.

## Data
Data comes from Kaggle Used Cars. Data was too big to load and was excluded from the repository.
Data can be found here:
https://mo-pcco.s3.us-east-1.amazonaws.com/BH-PCMLAI/module_11/practical_application_II_starter.zip

## Plots
Plots are not saved separately in this repository because of file size.

## Data Cleanup
VIN and id were disregarded as these were unique for each vehicle. Vehicle Model was disregarded for memory performance and we used manufacturer level aggregation only. Size was missing for more than 50% of the data and hence excluded.
Outliers for price and odometer were removed using IQR technique.
The code also includes another technique using DBSCAN but it is not implemented here.

## Script to run the code
Script can be found under Used-Car-Prices/prompt_II.ipynb

## Model
Models tested are limited to the ones learned so far in the program. Current models come from Sci-kit learn package. Future enhancement using more advanced models (such as RandomForest, XGBoost etc.) recommended.

## Finding based on model evaluation and validation
Our model can capture about 62% of variation in used car prices. We found age(manufacture year) and odometer(miles driven) to be the top two factors that determine the price of used cars. Fuel type and cylinder are other important factors. The model uses 10 features in total. Mean squared error, R squared values were used in conjunction with Grid Search CV to determine the best model. We used cross validation in additon to the hold out technique (train/test split). The best model uses ridge with alpha of 0.01.

This model was adjusted after evaluation of the previous best model which led to the dropping of two least important factors in determining price. 
