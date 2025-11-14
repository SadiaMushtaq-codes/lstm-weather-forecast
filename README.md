# Weather Forecasting Project

This project uses machine learning (specifically **LSTM neural networks**) to predict future weather temperatures based on historical data. The model is trained using a sequence of past temperature values and learns patterns over time to make accurate predictions.


## Project Description

This project focuses on **time-series forecasting** of temperature values for Hyderabad, Sindh. It takes past temperature data and predicts the next value.

###  Key Features

* Preprocessing of weather dataset
* Normalisation using MinMaxScaler
* Preparing sequences for LSTM
* LSTM model creation
* Training & evaluation
* Plotting actual vs predicted results


## Model Used: LSTM

LSTM (Long Short-Term Memory) is a type of recurrent neural network designed to learn time-dependent patterns. It is ideal for weather forecasting because weather depends on previous values.

 model:

* Uses one or more LSTM layers
* Uses Dense layer for final temperature output
* Learns from SEQ_LEN (sequence length) past data points


##  Requirements

Install the required libraries:

pip install numpy pandas matplotlib tensorflow scikit-learn

If using newer TensorFlow:

pip install tensorflow==2.17
```

(Compatible with Python 3.10.0)

---

## Input Data

The dataset should contain temperature values (in °F). Example:


## Data Preprocessing

* Load dataset using Pandas
* Select temperature column
* Convert to NumPy array
* Apply MinMaxScaler
* Create training sequences
* Split into train & test sets

---

## Training the Model

Inside the Jupyter notebook:

```
model.fit(X_train, y_train, epochs=20, batch_size=32)
```

* **Epochs:** how many times model sees full dataset
* **Batch size:** how many samples per gradient step

After training, the model is saved using:

```
model.save('weather_model.keras')
```

---

##  Results

plot:

* Actual vs Predicted temperatures
* Loss curve during training

Example code snapshot:

```
plt.plot(actual, label='Actual')
plt.plot(predicted, label='Predicted')
plt.legend()
plt.show()
```

---

## Model Evaluation

Metrics used:

* **MSE (Mean Squared Error)**
* **RMSE**

Example:

```
Global Test MSE: 0.0106
```

This tells how close predictions are to real values.

---

##  Future Improvements

You can add:

* Multi-feature input (humidity, wind speed, rainfall)
* Hyperparameter tuning
* GRU / deeper LSTM layers
* Flask web app for live weather predictions


##  Author

**Sadia Mushtaq**
Weather Forecasting using LSTM Neural Networks.
