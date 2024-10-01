# SBI_FutureStock_Analysis
Project Overview

This project leverages Long Short-Term Memory (LSTM) neural networks to predict future stock prices based on historical data from SBI (State Bank of India). The model predicts the next day and the next 10 days' stock prices, using the historical Open price as the primary feature.

Technologies Used
Python
Pandas
NumPy
Matplotlib
Scikit-learn
TensorFlow/Keras

Data
The dataset consists of historical stock data for SBI, particularly focusing on the Open price. Missing data is filled using forward fill, and the values are normalized using MinMaxScaler.
Model Architecture
LSTM with 2 layers:

50 units (with return_sequences=True) and 20 units.
Dropout (0.2) to prevent overfitting.
Dense layer for final prediction.
The model is trained using the Adam optimizer and mean_squared_error loss function.

Workflow

1. Data Preprocessing: Scaling and reshaping the Open price into sequences of 30 days.
2. Model Training: Trained for 30 epochs with a batch size of 20.
3. Prediction: Predicts stock prices for the next day and the next 10 days, and generates a plot comparing actual and predicted values.

How to Run

1. Install required libraries:
pip install pandas numpy matplotlib scikit-learn tensorflow

2. Clone the repository and run the script:
git clone https://github.com/your-username/stock-price-prediction-lstm.git
cd stock-price-prediction-lstm
python stock_price_prediction.py

Results
The script generates a plot comparing actual vs. predicted stock prices.
Predicts the next day's price and future 10 days' prices based on recent trends.


