# Building-a-Rainfall-Prediction-Classifier
Predicting rainfall in Melbourne using weather data and ML models like Random Forest and Logistic Regression. Includes preprocessing, GridSearchCV, model evaluation, and feature importance analysis.
# Melbourne Rain Prediction - Machine Learning Project

This project focuses on predicting whether it will rain tomorrow in the Melbourne area using machine learning. We utilize various machine learning models, including Random Forest and Logistic Regression, to create a classifier capable of predicting rain. The dataset used contains features related to weather conditions in Melbourne, such as temperature, humidity, wind speed, and more.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Installation](#installation)
- [Data Preprocessing](#data-preprocessing)
- [Modeling](#modeling)
- [Results](#results)
- [Model Comparison](#model-comparison)
- [License](#license)

## Project Overview
The goal of this project is to predict whether it will rain the next day based on various weather parameters. This type of prediction is useful in various fields like agriculture, event planning, and disaster management.

We use the following steps in this project:
1. **Data Preprocessing**: Clean and prepare the data for modeling.
2. **Modeling**: Train models such as Random Forest Classifier and Logistic Regression.
3. **Evaluation**: Assess the models based on their accuracy, precision, recall, and F1-score.
4. **Feature Importance**: Identify the most important features in predicting rainfall.
5. **Model Comparison**: Compare the performance of different models and choose the best one.

## Dataset
The dataset used in this project is the [Melbourne Rainfall Dataset](https://www.kaggle.com/datasets), which contains weather data for Melbourne. The dataset consists of the following features:
- `Date`: The date of observation.
- `MaxTemp`: The maximum temperature of the day.
- `MinTemp`: The minimum temperature of the day.
- `Rainfall`: The amount of rainfall recorded in mm.
- `Sunshine`: The amount of sunshine in hours.
- `WindGustDir`: The direction of the strongest wind gust.
- `WindGustSpeed`: The speed of the strongest wind gust.
- `Humidity9am`: The humidity level at 9 AM.
- `Humidity3pm`: The humidity level at 3 PM.
- `Pressure9am`: The pressure at 9 AM.
- `Pressure3pm`: The pressure at 3 PM.
- `Cloud9am`: The cloud cover at 9 AM.
- `Cloud3pm`: The cloud cover at 3 PM.
- `Temp9am`: The temperature at 9 AM.
- `Temp3pm`: The temperature at 3 PM.
- `RainTomorrow`: Whether it rained the next day (target variable).

## Installation
Follow the steps below to install the necessary dependencies and run the project:

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/melbourne-rain-prediction.git
    cd melbourne-rain-prediction
    ```

2. Create a virtual environment (optional but recommended):
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # For Linux/Mac
    venv\Scripts\activate     # For Windows
    ```

3. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

4. Run the project:
    ```bash
    python rain_prediction.py
    ```

## Data Preprocessing
Data preprocessing involved the following steps:
1. **Handling missing values**: Missing data was filled using imputation techniques for numeric and categorical values.
2. **Feature Engineering**: Some features were combined, and new ones were created to enhance the model's ability to predict.
3. **Categorical Encoding**: Categorical variables were encoded using one-hot encoding.
4. **Scaling**: Numerical features were standardized using `StandardScaler` to ensure they are on the same scale.

## Modeling
We used two main models for prediction:
1. **Random Forest Classifier**:
    - A powerful ensemble method that combines multiple decision trees to make predictions.
    - Tuned using `GridSearchCV` to find the optimal parameters.
    
2. **Logistic Regression**:
    - A simpler model that estimates the probability of an event (rain).
    - Regularization was applied to avoid overfitting.

## Results
The evaluation metrics for both models are summarized as follows:

### Random Forest Classifier:
- **Accuracy**: 84%
- **Precision (No Rain)**: 0.86
- **Precision (Rain)**: 0.76
- **Recall (No Rain)**: 0.95
- **Recall (Rain)**: 0.50
- **F1-Score (No Rain)**: 0.90
- **F1-Score (Rain)**: 0.60

### Logistic Regression:
- **Accuracy**: 83%
- **Precision (No Rain)**: 0.86
- **Precision (Rain)**: 0.69
- **Recall (No Rain)**: 0.93
- **Recall (Rain)**: 0.51
- **F1-Score (No Rain)**: 0.89
- **F1-Score (Rain)**: 0.59

### True Positive Rate (TPR) for Rain Prediction:
- **Random Forest Classifier**: 0.50
- **Logistic Regression**: 0.51

## Model Comparison
- **Accuracy**: Random Forest (84%) slightly outperforms Logistic Regression (83%).
- **Precision and Recall**: Random Forest performs better in precision for predicting rain (0.76 vs 0.69), but Logistic Regression has a higher recall for predicting no rain (0.93 vs 0.95).
- **Best Model**: Random Forest is considered the better model due to its slightly higher precision in detecting rain.

## Feature Importance
The top features that contribute to predicting rainfall include:
1. **Humidity3pm**: The most important feature for predicting rainfall.
2. **Pressure3pm**
3. **Temp3pm**
4. **Sunshine**

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

