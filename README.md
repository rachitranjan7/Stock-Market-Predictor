# Deep Learning Stock Prediction System 📈

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Deep%20Learning-FF6F00)
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)

A deep learning-based financial forecasting system that analyzes 20 years of historical stock market data using a Convolutional Neural Network (CNN). This project leverages time-series learning and automated pattern extraction to predict future stock price behavior and visualize market trends.

---

# 📖 Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Key Features](#key-features)
- [Project Architecture](#project-architecture)
- [Installation & Usage](#installation--usage)
- [Results](#results)
- [Built With](#built-with)
- [License](#license)

---

# 🔍 Overview

Financial markets generate massive amounts of sequential data that contain hidden temporal patterns, momentum shifts, volatility spikes, and trend reversals. Traditional statistical models often struggle to capture these complex nonlinear relationships.

This project builds a deep learning pipeline using a 1D Convolutional Neural Network (CNN) to automatically learn short-term temporal structures directly from historical stock prices. By training on rolling time windows of historical market behavior, the model forecasts future stock price movements and visualizes prediction accuracy against real-world market trajectories.

---

# 📊 Dataset

This project uses historical stock market data downloaded dynamically using the Yahoo Finance API through the `yfinance` Python library.

* **Data Source:** Yahoo Finance
* **Historical Range:** ~20 years of daily market data
* **Features Used:**
  - Open Price
  - High Price
  - Low Price
  - Close Price
  - Trading Volume

* **Prediction Target:** Next-day closing price forecasting

---

# ✨ Key Features

* **Automated Financial Data Collection:** Dynamically downloads historical stock data using `yfinance`.

* **Time-Series Sequence Generation:** Converts continuous stock data into rolling historical windows suitable for deep learning models.

* **CNN-Based Pattern Recognition:** Uses 1D convolutional layers to automatically detect local temporal market patterns such as:
  - Momentum shifts
  - Short-term trends
  - Price reversals
  - Volatility spikes

* **Feature Scaling & Preprocessing:** Implements MinMax normalization for stable neural network convergence.

* **Prediction Visualization:** Generates detailed comparisons between actual stock trajectories and CNN-generated forecasts.

* **Future Price Forecasting:** Predicts the next trading day's closing price using the latest historical sequence.

---

# 🧠 Project Architecture

1. **Data Collection:** Download and preprocess historical stock market data.

2. **Normalization:** Scale financial features using `MinMaxScaler`.

3. **Sequence Construction:** Convert continuous time-series data into rolling 60-day input windows.

4. **CNN Feature Extraction:** Learn local temporal structures using Conv1D layers.

5. **Model Training:** Optimize the network using Mean Squared Error (MSE) loss and the Adam optimizer.

6. **Evaluation & Forecasting:** Compare predicted stock prices against actual market behavior and forecast future trends.

---

# 🚀 Installation & Usage

This project is optimized to run in **Google Colab** with minimal setup.

## 1. Clone this repository

```bash
git clone https://github.com/yourusername/Stock-Prediction-System.git
cd Stock-Prediction-System
```

## 2. Open the notebook

Open the notebook in **Google Colab** or **Jupyter Notebook**.

## 3. Install dependencies

Run the first notebook cell:

```bash
!pip install yfinance tensorflow scikit-learn pandas numpy matplotlib seaborn
```

## 4. Run the pipeline

Execute the notebook cells sequentially to:
- Download stock data
- Preprocess the dataset
- Train the CNN model
- Generate predictions
- Visualize results

---

# 📈 Results

The CNN model successfully learns temporal market behavior and captures short-term price movement patterns from historical financial data.

The project visualizes:
- Actual vs Predicted stock prices
- Training and validation loss curves
- Future next-day stock forecasts

Below is a sample visualization comparing actual market prices with CNN-generated predictions.

![Prediction Results](docs/stock_prediction_results.png)

---

# 🛠️ Built With

- [TensorFlow](https://www.tensorflow.org/) — Deep learning framework for CNN modeling  
- [Scikit-learn](https://scikit-learn.org/) — Data preprocessing and evaluation metrics  
- [yfinance](https://github.com/ranaroussi/yfinance) — Yahoo Finance market data API  
- [Pandas](https://pandas.pydata.org/) & [NumPy](https://numpy.org/) — Data manipulation and numerical computation  
- [Matplotlib](https://matplotlib.org/) & [Seaborn](https://seaborn.pydata.org/) — Financial data visualization  

---

# 📄 License

![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.
