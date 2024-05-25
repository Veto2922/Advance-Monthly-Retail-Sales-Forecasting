
# Advance Monthly Retail Sales Forecasting

## Overview

This project involves forecasting the monthly sales for clothing and clothing accessory stores using LSTM (Long Short-Term Memory) neural networks. The dataset consists of monthly sales data (in millions of dollars, not seasonally adjusted) retrieved from the FRED, Federal Reserve Bank of St. Louis.

## Data Source

**Release:** Advance Monthly Sales for Retail and Food Services  
**Units:** Millions of Dollars, Not Seasonally Adjusted  
**Frequency:** Monthly

The value for the most recent month is an advance estimate based on a subsample of firms from the larger Monthly Retail Trade Survey. This estimate will be revised in subsequent months with data from the full survey.

- **Dataset URL:** [Advance Retail Sales: Clothing and Clothing Accessory Stores](https://fred.stlouisfed.org/series/RSCCASN)
- **Further Information:** [Advance Monthly Retail Sales Survey](https://www.census.gov/retail/marts/about_the_surveys.html)

## Suggested Citation

U.S. Census Bureau, Advance Retail Sales: Clothing and Clothing Accessory Stores [RSCCASN], retrieved from FRED, Federal Reserve Bank of St. Louis; [FRED Series RSCCASN](https://fred.stlouisfed.org/series/RSCCASN), November 16, 2019.

## Project Steps

### 1. Data Preparation

- Load the dataset using Pandas.
- Parse dates and set the date column as the index.
- Rename the column to 'Sales'.
- Plot the data for visualization.

### 2. Train-Test Split

- Split the data into training and test sets.
- The test set covers the last 24 months for forecasting.

### 3. Data Scaling

- Scale the data using MinMaxScaler from scikit-learn to normalize the data.

### 4. Time Series Generator

- Use the TimeseriesGenerator from Keras to create sequences for the LSTM model, which helps in generating training and validation batches.

### 5. Model Creation

- Create an LSTM model using Keras.
- Add layers to the model, including LSTM and Dense layers.
- Compile the model with an appropriate optimizer and loss function.

### 6. Model Training

- Train the model using the training and validation generators.
- Use early stopping to prevent overfitting by monitoring validation loss.

### 7. Model Evaluation

- Evaluate the model on the test data.
- Make predictions and plot the results to compare predicted values with actual values.

### 8. Retrain and Forecast

- Retrain the model on the full dataset.
- Forecast future values and plot these predictions to visualize the forecast against historical data.

## Dependencies

- Python 3.x
- pandas
- numpy
- matplotlib
- scikit-learn
- tensorflow
- keras

## How to Run

1. Ensure all dependencies are installed.
2. Place the dataset in the appropriate directory.
3. Run the script to preprocess data, train the model, and generate forecasts.

## Conclusion

This project demonstrates the use of LSTM neural networks for time series forecasting. The model is trained on historical sales data and is able to predict future sales with reasonable accuracy.

---
