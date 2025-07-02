 # PJM Hourly Energy Consumption Forecast

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This repository contains a time-series analysis and forecasting project to predict hourly energy consumption in the PJM (Pennsylvania-New Jersey-Maryland) region. The project compares the performance of two popular forecasting models: **XGBoost** and **Facebook's Prophet**.

The analysis is based on the [PJM Hourly Energy Consumption dataset](https://www.kaggle.com/datasets/robikscube/hourly-energy-consumption) from Kaggle, which spans from 2002 to 2018.

## 🎯 Objective

The primary goal of this notebook is to apply machine learning techniques to accurately forecast future energy usage. The key objectives are:

*   To identify and visualize trends, seasonality, and anomalies in energy consumption data.
*   To engineer relevant time-series features to improve model accuracy.
*   To build, train, and evaluate both an XGBoost and a Prophet model.
*   To compare their predictive capabilities and determine their effectiveness for this specific forecasting task.

## 🛠️ Tech Stack & Libraries

This project is built using Python and several key data science libraries:

*   **Data Manipulation & Analysis**: `pandas`, `numpy`
*   **Data Visualization**: `matplotlib`, `seaborn`
*   **Machine Learning & Forecasting**: `scikit-learn`, `xgboost`, `prophet`
*   **Environment**: Jupyter Notebook

## 🚀 Getting Started

To run this project on your local machine, follow these steps.

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/sandiindika/PJM-Forecast-Model-Comparison.git
    cd PJM-Forecast-Model-Comparison
    ```

2.  **Create and activate a virtual environment:**
    ```bash
    # Create the environment
    python -m venv venv

    # Activate on Windows (PowerShell)
    .\venv\Scripts\Activate.ps1

    # Activate on macOS/Linux
    source venv/bin/activate
    ```

3.  **Install the required dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
    Then, open the `notebook.ipynb` file from the Jupyter interface in your browser.

## 📊 Results & Model Performance

*   **Exploratory Data Analysis (EDA)** revealed strong daily, weekly, and yearly seasonality in energy consumption.
*   **Feature Engineering**: Time-series features such as hour, day of the week, month, and year were created. US federal holidays were also incorporated as a feature.
*   **Model Comparison**:
    *   The **XGBoost Regressor** was trained on the engineered features.
    *   It achieved a **Mean Absolute Percentage Error (MAPE) of 9.04%** on the test set (2015-2018).
    *   The most important features for the XGBoost model were `hour`, `dayofyear`, and `month`.

*(Note: The notebook also includes the setup for a Prophet model, providing a framework for direct performance comparison.)*

## 📄 License

This project is licensed under the MIT License.