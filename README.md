# Machine-Learning-Codeathon---Intermediate-Assessment


Car Price Prediction Using Regression

Project Overview

This project is about predicting car prices using different machine learning regression models.

The dataset contains information about cars in the American market. The main goal is to find out which car features have the biggest effect on price and build a model that can predict car prices.

Dataset

The dataset contains 205 records and 26 columns
The target variable is price

Some of the features include:

* Fuel type
* Car body
* Drive wheel
* Engine size
* Horsepower
* Curb weight
* Mileage
* Car width and length

Preprocessing

The dataset was checked for missing values and duplicates. The car brand was extracted from CarName, and unnecessary columns were removed

Categorical variables were encoded using OneHotEncoder, and numerical variables were scaled using StandardScaler

The data was split into **80% training** and **20% testing** data.

Models Used

The following five regression models were used:

1. Linear Regression
2. Decision Tree Regressor
3. Random Forest Regressor
4. Gradient Boosting Regressor
5. Support Vector Regressor

## Model Evaluation

The models were compared using R², MSE, and MAE.

| Model             |         R² |           MSE |       MAE |
| ----------------- | ---------: | ------------: | --------: |
| Linear Regression |     0.8998 |     7,906,808 |     1,835 |
| Decision Tree     |     0.9136 |     6,820,817 |     1,704 |
| **Random Forest** |     0.9578 |     3,334,668 |     1,287 |
| Gradient Boosting |     0.9282 |     5,671,210 |     1,691 |
| SVR               |    -0.0998 |    86,821,850 |     5,695 |

Best Model

Random Forest Regressor performed the best because it had the highest R² and the lowest MSE and MAE.

Feature Importance

Feature importance was checked using the Random Forest model. Some of the important features were:

* Engine size
* Curb weight
* Horsepower
* Car width
* City and highway mileage

Hyperparameter Tuning

GridSearchCV was used to tune the Random Forest model by testing different values for n_estimators, max_depth, and min_samples_split.

For this dataset, the tuned model did not improve the test performance, so the original Random Forest model was kept as the final model.

Conclusion

Overall, Random Forest Regressor was the best model for predicting car prices in this project. The feature analysis also helped identify the main factors that influence car prices.
