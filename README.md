# Bike-ride-request-forecast

```
# Bike Count Prediction

This project predicts the number of rented bikes based on weather and environmental factors. The model utilizes multiple machine learning algorithms, such as Linear Regression, Random Forest, XGBoost, and more to predict the bike count in Seoul, Korea.

## Project Setup

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/bike-count-prediction.git
   cd bike-count-prediction
   ```

2. **Install required packages**:
   You can install the necessary libraries by running the following command:
   ```bash
   pip install -r requirements.txt
   ```

3. **Dataset**:
   The project uses the `SeoulBikeData.csv` file, which contains historical weather data for Seoul, Korea, as well as bike rental counts.

4. **Project Structure**:
   - `SeoulBikeData.csv`: The dataset used for training and predictions.
   - `bike_count_prediction.py`: The main script that contains data preprocessing, model training, and evaluation.
   - `app.py`: The Gradio web app for real-time bike count prediction.

## How the Code Works

### Data Preprocessing

- The dataset is cleaned by removing unnecessary columns like `Date`, `Functioning Day`, and `Holiday`.
- The "Seasons" and "Holiday" columns are encoded using `LabelEncoder`.
- The `Day`, `Month`, `Year`, and `Weekday` columns are extracted and processed.
- Outliers are removed based on specific conditions for `Wind speed (m/s)` and `Humidity(%)`.

### Feature Engineering

- Features like temperature, humidity, wind speed, visibility, and solar radiation are used to predict the rented bike count.
- Various columns like `Seasons`, `Holiday`, `Year`, and `Weekday` are also taken into account for the prediction.

### Model Training

- The dataset is split into training and validation sets.
- Multiple machine learning models are trained, including:
  - Linear Regression
  - XGBoost Regressor
  - Lasso
  - Random Forest Regressor
  - Ridge Regression

- The performance of each model is evaluated using Mean Absolute Error (MAE).

### Gradio Web App

A Gradio interface is used for real-time bike count predictions. The user provides inputs such as:
- Temperature (°C)
- Humidity (%)
- Wind speed (m/s)
- Visibility (10m)
- Dew point temperature (°C)
- Solar radiation (MJ/m²)
- Rainfall (mm)
- Snowfall (cm)
- Season (Winter, Spring, Summer, Autumn)
- Holiday status (Holiday, No Holiday)
- Company functioning status (Yes, No)
- Selected Model (Linear Regression, XGBRegressor, Lasso, RandomForest, Ridge)

The model predicts the number of bikes rented based on the provided inputs.

### Running the Web App

To launch the Gradio web app, run the following command:

```bash
python app.py
```

This will start the app and provide a link to open in your browser, where you can input the required values and get the bike rental predictions.

## Requirements

- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `xgboost`
- `gradio`

You can install all required libraries using the following command:

```bash
pip install -r requirements.txt
```

## Conclusion

This project provides a machine learning model for predicting bike rental counts in Seoul based on environmental factors. By utilizing different machine learning algorithms and preprocessing techniques, the model is capable of providing accurate predictions.

```
