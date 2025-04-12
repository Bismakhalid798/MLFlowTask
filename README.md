Wine Quality Prediction with ElasticNet & MLflow

This project demonstrates how to train a machine learning model to predict wine quality using physicochemical properties. The model is trained using ElasticNet regression, and MLflow is used for experiment tracking and model logging.

Dataset:
The dataset used in this project is the [Wine Quality DataSet](https://archive.ics.uci.edu/ml/datasets/Wine+Quality) from the UCI Machine Learning Repository.
Reference:
P. Cortez, A. Cerdeira, F. Almeida, T. Matos, and J. Reis.
Modeling wine preferences by data mining from physicochemical properties.
In Decision Support Systems, Elsevier, 47(4):547-553, 2009.

How It Works:
The script performs the following steps,

Downloads the dataset (Red Wine quality data).
Splits the data into training and test sets.
Trains an ElasticNet regression model.
Evaluates the model using RMSE, MAE, and R² score.
Logs parameters, metrics, and the model using MLflow.
Optionally registers the model if the tracking server is not a local file store.

Evaluation Metrics:
The model performance is evaluated using:
RMSE (Root Mean Squared Error)
MAE (Mean Absolute Error)
R² Score

Requirements:
Install the required Python packages:
pip install pandas numpy scikit-learn mlflow

Usage:
You can run the script with default parameters:
python wine_quality_elasticnet.py

Or specify alpha and l1_ratio:
python wine_quality_elasticnet.py 0.3 0.7

MLflow Tracking:
To start an MLflow UI for visualizing experiments:
mlflow ui

Notes:
The model uses ElasticNet regression due to its regularization properties which balance L1 and L2 penalties.
The dataset includes various physicochemical properties (e.g., acidity, sugar, pH) and the target variable is the wine quality score (rated 0–10).
MLflow’s model registry functionality is only used if the tracking URI is not a local file store.
