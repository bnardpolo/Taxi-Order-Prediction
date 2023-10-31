# Taxi-Order-Prediction
Taxi Order Prediction using Data science
## Project Description
The Sweet Lift Taxi company has amassed a substantial amount of historical data regarding taxi orders at airports. In order to attract more drivers during peak hours, the company seeks to predict the number of taxi orders for the upcoming hour. The primary goal of this project is to build a predictive model for this purpose.

The project aims to achieve a Root Mean Square Error (RMSE) metric on the test set that does not exceed 48, indicating the accuracy and reliability of the predictive model.

## Project Instructions
To achieve the goal of predicting taxi orders effectively, follow these instructions:

1. **Data Collection and Preprocessing**:
    - Download the dataset, which is stored in the 'taxi.csv' file.
    - Resample the data to one-hour intervals to make it suitable for time-series analysis.

2. **Data Analysis**:
    - Perform an in-depth analysis of the resampled data to gain insights into the trends, patterns, and characteristics of taxi orders.

3. **Model Building and Testing**:
    - Train various predictive models using different hyperparameters to find the most suitable one.
    - The test sample should be 10% of the initial dataset to evaluate model performance.
    - Calculate the RMSE for each model on the test data.

4. **Conclusion**:
    - Summarize the findings and insights from the data analysis.
    - Report the performance of the different models and explain why one model was selected as the best choice for predicting taxi orders.

## Data Description
The dataset, 'taxi.csv,' contains historical information about taxi orders. The key information to note is that the number of orders is found in the 'num_orders' column.

**Key Findings**:
1. The dataset spans from 2018-03-01 to 2018-08-31, capturing a total of 26,496 orders at 10-minute intervals.
2. There are no duplicates or missing values in the dataset.
3. The data is time-ordered, and there are no gaps.
4. The mean number of orders is 14, ranging from 0 to 119.

**Temporal Trends**:
1. A daily pattern is observed where the mean order count drops between 5 AM and 7 AM, consistent throughout the week.
2. Midnight (12 AM) exhibits a higher-than-average number of orders compared to other hours.
3. Between 8 AM and 8 PM, the number of rides is around the mean of 15.

**Time-Series Analysis**:
1. The trend plot displays an upward trend.
2. A daily seasonal pattern is evident, peaking at 12 AM and reaching its lowest point at 6 AM.
3. The residuals show that the mean is not 0, suggesting a potential bias in predictions.
4. Seasonal analysis for one day indicates increased ridership frequency at midnight, a drop to the lowest level at 6 AM, and a moderate rise around 5 PM.

## Model Selection
Three different models were trained and tested using grid search based on the number of iterations and depth size, utilizing 5-fold time-series cross-validation. The CatBoostRegressor model emerged as the top-performing model with the lowest RMSE, despite having a longer training time (780 seconds).

## Summary
In summary, this project involves predicting taxi orders for Sweet Lift Taxi company during peak hours at airports. The data analysis reveals temporal trends, and time-series analysis identifies daily seasonal patterns. The CatBoostRegressor model is chosen as the best predictive model, offering accurate predictions but requiring longer training time. This model can assist Sweet Lift Taxi in attracting more drivers during peak hours, enhancing their service, and optimizing resource allocation.
