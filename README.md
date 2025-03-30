# Stock Price Prediction Using LSTM and GRU Models

### Overview

This project aims to predict stock prices using LSTM (Long Short-Term Memory) and GRU (Gated Recurrent Unit) models, two advanced deep learning techniques specifically designed for time series forecasting. The project leverages historical stock price data, including features like Open, High, Low, Close, Adjusted Close, and Volume, to build predictive models that forecast future stock prices.

### Dataset

The dataset used for this project contains historical stock price data for various companies. Metadata:

- Ticker: Stock ticker symbol (e.g., 'A' for Apple)
- Date: The date of the stock price
- Open: The opening price of the stock for that day
- High: The highest price of the stock during that day
- Low: The lowest price of the stock during that day
- Close: The closing price of the stock for that day
- Adj Close: The adjusted closing price, accounting for stock splits and dividends
- Volume: The number of shares traded on that day

The dataset contains 5964 entries across 8 columns.

### Steps Involved

1. Data Preprocessing:
- Data cleaning: Handle missing values (if any).
- Date formatting: Convert Date to datetime format.
- Feature scaling: Normalize the data using MinMaxScaler to bring all features into the range [0, 1].
- Time-series formatting: Create sequences of past stock prices as features to predict the future stock prices.

2. Model Building:
- LSTM (Long Short-Term Memory): A type of Recurrent Neural Network (RNN) that is effective for time-series forecasting due to its ability to capture long-term dependencies.
- GRU (Gated Recurrent Unit): A simpler alternative to LSTM, often providing similar performance with fewer parameters.

3. Model Training:
- Split the data into training and validation sets.
- Train the models using the training set and evaluate the performance using the validation set.
- Monitor the loss (MSE) and MAE (Mean Absolute Error) over the epochs.

4. Model Evaluation:
- Evaluate the models based on validation loss and validation MAE.
- Compare the performance of the LSTM and GRU models.

5. Evaluation Metrics
- Mean Absolute Error (MAE): Measures the average magnitude of errors in predictions, regardless of direction.
- Mean Squared Error (MSE): Measures the average of the squares of the errors, penalizing larger errors more.

### Results

The LSTM model shows steady improvement and generalizes well to the validation set, making it a strong candidate for forecasting stock prices. The LSTM model demonstrated superior performance in stock price prediction, with lower validation MAE and loss compared to the GRU model. It is suitable for deployment in forecasting stock prices.

The GRU model performed less well than LSTM, with higher loss values and MAE. The GRU model showed high initial loss, which decreased over time, but it still lagged behind the LSTM model in terms of performance. The GRU model, although improving over epochs, did not reach the level of performance seen in the LSTM model. It might require further tuning or a more suitable architecture for time-series forecasting.

### Future Work

1. Hyperparameter Tuning: Fine-tuning both models to optimize their performance.

2. Feature Engineering: Adding more features such as moving averages, volatility, and sentiment analysis to improve the model.

3. Ensemble Models: Combining the predictions from multiple models (e.g., LSTM and GRU) to enhance accuracy.

4. Evaluation on Multiple Stocks: Expanding the analysis to include multiple stock tickers for broader forecasting applications.

### Source

![S&P 500 Stock Data From Listing Day to 2023 from Kaggle](https://www.kaggle.com/datasets/pavankrishnanarne/s-and-p-500-stock-data-from-listing-day-to-2023)
