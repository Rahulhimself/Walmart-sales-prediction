Walmart Sales Prediction
Project Overview
This project focuses on predicting weekly sales for different Walmart stores using historical sales data. By leveraging various machine learning models and analyzing key features such as store location, promotional events (holidays), and temperature, we aim to build a robust model that can accurately forecast future sales. The goal is to provide actionable insights for business planning sales for supply and demand stratergy and inventory management.

The Data
The dataset contains historical sales data for 45 Walmart stores, covering a period of over two years. The key features in the dataset include:

Store: The unique identifier for each store.

Date: The week of sales data.

Weekly_Sales: The target variable to be predicted.

Holiday_Flag: A boolean indicating whether the week includes a special holiday (e.g., Super Bowl, Christmas).

Temperature: Average temperature in the region.

Fuel_Price: Cost of fuel in the region.

CPI: Consumer Price Index.

Unemployment: Unemployment rate in the region.

Methodology
1. Data Preprocessing & Feature Engineering
The raw data was preprocessed to handle missing values and prepare it for modeling. New features were engineered from the existing data to capture seasonality and time-based trends. This included extracting features like Day_of_Week, Month, and Year from the Date column.

2. Exploratory Data Analysis (EDA)
Initial analysis was performed to understand the relationships between different variables. Key findings included:

Sales exhibit strong seasonal patterns, with clear peaks around major holidays.

Certain stores consistently perform better than others, indicating the importance of the Store feature.

There are noticeable correlations between sales and factors like Temperature and Unemployment.

3. Model Training & Selection
A variety of time series models were trained and evaluated to find the best fit for this problem. The following models were considered:

Linear Regression: A simple baseline model.

Random Forest Regressor: An ensemble model known for its high accuracy and ability to capture non-linear relationships.

ARIMA: The AutoRegressive Integrated Moving Average (ARIMA) model, a popular and powerful statistical method for time series forecasting.
The data was split into training and validation sets, and k-fold cross-validation was used to ensure the model's performance was consistent and not overfitting to a single data split.

4. Evaluation
The primary metric used to evaluate the models was the Root Mean Squared Error (RMSE). This metric measures the average magnitude of the errors between predicted and actual sales, providing a clear indication of the model's predictive accuracy.

Results
The ARIMA model consistently outperformed other models, achieving the lowest RMSE on the validation set. This model was selected as the final predictive model. The feature importance analysis revealed that the Store number, unemployment, and Holiday_Flag were the most significant predictors of weekly 

Project Structure

FIRST PART CONTAINS EDA AND VISUALIZATION DEPENDING UPON THE FACTORS AFFECTING SALES SUCH AS HOLIDAY FLAGS, TEMP, UNEMPLOYMENT etc

SECOND PART--PREDICTIVE ANALYSIS CONTAINS THE PATH

├── data/

│   ├── train.csv

│   └── test.csv

├── notebooks/

│   └── sales_prediction_analysis.ipynb

├── src/

│   ├── preprocess.py

│   ├── model.py

│   └── predict.py

├── requirements.txt

└── README.md


data/: Contains the raw and processed datasets.

How to Run
Clone the repository:

git clone [https://github.com/Rahulhimself/Walmart-sales-prediction.git](https://github.com/Rahulhimself/Walmart-sales-prediction.git)
cd Walmart-sales-prediction


Install dependencies:

pip install -r requirements.txt


Run the prediction script:

python src/predict.py


Dependencies
The project was developed using Python and the following libraries:

pandas

numpy

scikit-learn

prophet

matplotlib

seaborn

ARIMA

Future Improvements:

Integrate external data sources such as local events or competitor pricing.

Experiment with advanced deep learning models like LSTMs for time series forecasting.

Deploy the model as an API for real-time sales predictions.
