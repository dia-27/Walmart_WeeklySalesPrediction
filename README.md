# Walmart data weekly sales prediction

This notebook shows weekly sales prediction for Walmart based on available historical data.





## Data

**train.csv** - CSV Data file containing following attributes
- Store
- Dept
- Date
- Weekly_Sales
- IsHoliday

**stores.csv** - CSV Data File containing following attributes
- Store
- Type
- Size

**features.csv** - CSV Data file containing following attributes
- Store
- Date
- Temperature
- Fuel_Price
- MarkDown1
- MarkDown2
- MarkDown3
- MarkDown4
- MarkDown5
- CPI
- Unemployment
- IsHoliday

## Data Preprocessing

#### Merging datasets
- Stores.csv, Features.csv, train.csv merged to get the final dataset.
- Final dataset contains rows 421570 and 15 attributes.

#### Filling Null values
- Markdown1, Markdown2, Markdown3, Markdown4, Markdown5 contains 4158, 5269, 4577, 4726, 4140 null values respectively.These are filled by zeros.

- CPI and Unemployment contains 585 null values which are filled by mean of the respective column.

#### One- Hot Encoding
Columns Type and IsHoliday are one hot encoded by using pandas.get_dummies.

#### Normalization
Numerical columns normalized using StandardScaler.

## Splitting dataset
- Dataset was splittedas 80% for training and 20% for testing.
- Weekly_Sales is the target variable.

## Models used 
- K- Neighbours Regression
- Random Forest Regressor


