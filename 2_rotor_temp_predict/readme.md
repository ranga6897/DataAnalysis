The file your watching has small trick in it, instead of loading the images from notebook excuted, i used saved images which don't have javascript functionality in plolty plots.        
Because the orginal file size is 300 mb and does not load in github. 
[original files](https://drive.google.com/drive/folders/1DypfDOYXhSY6vpila0H_pJrOo5DVD5ri?usp=sharing)

**Objective** :                  
To build a model that predicts the rotor temperature.

**Data** :                   
Data is taken [kaggle](https://www.kaggle.com/wkirgsn/electric-motor-temperature), Data is anonymized.

**Work Done** :
1. EDA - checked the attributes to different test cases
2. Feature Selection - Using KBeast, Pearson correlation coefficient and Bartlett variance test.
3. Model Building :
| model |mse|splits|
|---|---|---|
|Stats OLS | 0.225 | 0
| LinearReg  | 0.475260(+- 0.000616) |3 |
|RandomForest | 0.033642(+- 0.001383) |3 |
|AdaBoost LinearReg as base | 0.500461(+- 0.010645) |3 |
|AdaBoost DT as base | 0.552619(+- 0.000956) |3 |
|GBoost  | 0.398417(+- 0.000631) |3 |
|KNeighborsRegressor |**0.003927(+- 0.000068)** |3 |

* The Best model is KNeighborsRegressor with parameters : Metric = Euclidean, n_neighbours = 2, weights = distance.
   


**Work can be done**:

1.EDA :                  
As the given data is anonymized and we have 57 test_cases, We can find similar test cases (eg : profile_id's : 46 to 69 can be treated as one test_group and create a catagorical column)

2.Model :                   
   * Tuning Hyper parameters for RF
   * Checking tree graph of DT to understand on what factors it's predicting.