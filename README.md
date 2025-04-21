# lsmt-models-stock-market
Recurrent Neural Networks (RNNs) or LSTM models to learn from sequences of past data to predict the future using yfinance for stock market!
---

#Data Collection & Preparation
- Fetched historical stock data via the `yfinance` library  
- Selected the ‘Close’ price as the feature to model  
- Normalized values with `MinMaxScaler` to the [0,1] range  
- Created input sequences of length 100 (i.e. used the previous 100 days to predict the next day)
  
---

#Model Architecture & Training
- Built an LSTM neural network in Keras/TensorFlow consisting of:  
  - Two LSTM layers (50 units each)  
  - One intermediate Dense layer  
  - One output Dense layer for the forecasted value  
- Compiled with the Adam optimizer and mean squared error loss  
- Trained for 100 epochs on the training set

---

#Prediction & Visualization
- Generated predictions on the test set  
- Inverse‑transformed predictions back to original price scale  
- Plotted actual vs. predicted prices using Matplotlib for performance assessment

---

#Streamlit App Deployment
- Wrapped the pipeline in a Streamlit interface that lets users:  
  - Input a stock ticker and date range  
  - View the raw historical data table  
  - See line charts of actual vs. predicted prices  
  - Interact with real‑time model output directly in the browser

---
