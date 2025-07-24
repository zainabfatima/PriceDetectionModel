SARIMAX-Based LNG Price Prediction
A time series forecasting project that leverages the SARIMAX model to predict LNG (Liquefied Natural Gas) prices based on historical consumption data.

🚀 Features
Reads and preprocesses real LNG data

Handles outlier removal and data smoothing

Time series resampling and imputation

Detects seasonality and trend

Splits data into training/testing

Builds and fits a SARIMAX model

Forecasts future values (till ~2031!)

Evaluation via MSE, RMSE, and visualization

🧠 How It Works
Dataset (CSV) is loaded using pandas

Missing values handled, outliers removed using IQR

Data is resampled daily and smoothed using a rolling mean

The model uses:

SARIMAX(order=(2,1,1), seasonal_order=(1,1,2,24))

Predictions are made on test data

Future forecasting is extended using .forecast(steps=n)

Forecasted values are aggregated yearly and visualized

📂 Project Structure
pgsql
Copy
Edit
Sarimax-Lng-Prices-Prediction/
├── Predicting_LPG_prices.ipynb     # Complete end-to-end pipeline notebook
├── TimeSeries (1).ipynb            # Additional experiments or older version
├── README.md                       # Project overview and usage
⚙️ Requirements
bash
Copy
Edit
pip install pandas numpy matplotlib statsmodels scikit-learn plotly
▶️ How to Run
Clone the repository:

bash
Copy
Edit
git clone https://github.com/moaaz12-web/Sarimax-Lng-Prices-Prediction
cd Sarimax-Lng-Prices-Prediction
Open the notebook:

Use Jupyter or Google Colab to open:

bash
Copy
Edit
Predicting_LPG_prices.ipynb
Upload your CSV (or use provided dataset)

Make sure your CSV file has date and numerical value columns like:

yaml
Copy
Edit
Column1.load_start_date,LNG converted (total)
2022-01-01, 1000
2022-01-02, 1050
...
📤 Input Format
A CSV with two columns:

Column1.load_start_date: Date

LNG converted (total): Numeric value (e.g., consumption)

📈 Output
Cleaned and smoothed time series

Predicted vs Actual comparison plots

Forecasted future values plotted until 2031+

Year-wise aggregated forecast data

Evaluation Metrics:

MSE

RMSE
