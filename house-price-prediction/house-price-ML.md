# Decision Trees and Random Forest ~ House Price Predictor 
This project focuses on predicting house prices using a dataset containing various features and attributes to residential properties using decision tree and random forest. By analysing and modelling the data, the project aims to develop a predictive model that can estimate the sale prices of houses accurately.

## Dataset Information
The dataset used in this project consists of information about different residential properties. It includes a wide range of features that can potentially influence the price of a house, such as the number of bedrooms, bathrooms, square footage, location, neighborhood characteristics, and other relevant factors.

## Step by step project breakdown:

### 1. Basic Data Exploration:
- First, install relevant python libraries, I will be using Pandas for this project
 ```python
    import pandas as pd
```
import path to find file to read using function ``` .read_csv() ```: 
```python
house_price_path = "/Users/heyjowaria/Downloads/data_science/dataset/train.csv"
house_price = pd.read_csv(house_price_path)
```
drop any missing value variables using function ``` .dropna() ```
```python
house_price = house_price.dropna(axis= 0)
```
select the prediction target: in this project i selected SalePrice as i am looking at predicting house prices:
```python
y = house_price.SalePrice
```
choosing the features to create X: the columns that are inputted into the model (and used to make predictions) are called 'features'. in this case, the features are used to determine the home price.
```python
house_price_features = ['LotArea', 'YearBuilt', '1stFlrSF', '2ndFlrSF', 
'FullBath', 'BedroomAbvGr', 'TotRmsAbvGrd']
```

select data corresponding to features in features names
```python
X = house_price[house_price_features]
```
