### Objective :                  
To build a model that predicts the price of used cars.

### Data :                   
Data is taken from [kaggle](https://www.kaggle.com/doaaalsenani/usa-cers-dataset).


### Work Done :
1. Pre-Processing 
    - Formatting data in columns, deleting unique cols, replacing values with least value_counts to others.
2. Outliers:
     - 43 cars have **price = 0**, which was due to salvage_insurance.
     - Used **Isolation Forest** to check for outliers.
3. EDA :
     - Checked price variation of Same model car in different states with their respective age.
     - Checked price variation in different brands.
  
4. Model Building :

| Model | mse |splits|
|------|------|------|
| KNeighborsRegressor  | **0.45(+-0.063)** | 3 |
|RandomForest Regressor | 0.56(+-0.064) | 3 |
| AdaBoost | 0.81(+-0.03) |3 |
| GradientBoost | 0.60(+-0.05) |3 |
