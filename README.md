# Electrical Load Forecasting

## 📌 Project Overview
This project implements and compares three different time-series forecasting models for electrical load prediction:
1. **Holt-Winters Exponential Smoothing**
2. **Facebook Prophet**
3. **Long Short-Term Memory (LSTM) Neural Network**

The system forecasts electricity demand for short to medium terms, which is crucial for power grid management, resource planning, and operational efficiency in the energy sector.

## 🎯 Key Features
- **Multi-model approach** comparing traditional, modern, and deep learning techniques
- **Web application interface** for easy forecasting
- **High accuracy predictions** (up to 92% accuracy)
- **Comprehensive data preprocessing** and feature engineering
- **Visualization of forecasts** with comparative analysis

## 📊 Models Implemented

### 1. Holt-Winters Exponential Smoothing
- Traditional time-series forecasting method
- Models level, trend, and seasonality components
- Accuracy: 86%

### 2. Facebook Prophet
- Robust forecasting procedure developed by Facebook's Core Data Science team
- Handles missing data, trend changes, and outliers effectively
- Models holidays and seasonal patterns
- Accuracy: 91%

### 3. LSTM (Long Short-Term Memory)
- Deep learning approach using recurrent neural networks
- Captures long-term dependencies in time-series data
- Three-gate architecture (Forget, Input, Output gates)
- Accuracy: 92%

## 🏗️ System Architecture

### Data Pipeline:
1. **Data Collection** - Historical electricity consumption data
2. **Preprocessing** - Cleaning, normalization, feature extraction
3. **Feature Engineering** - Creating temporal features (hour, day, month, year, etc.)
4. **Model Training** - Training three different forecasting models
5. **Evaluation** - Comparing results using error metrics
6. **Deployment** - Web application for real-time forecasting

### Web Application:
- **Frontend**: HTML, CSS
- **Backend**: Python with Flask/Django framework
- **Deployment**: ngrok for tunneling

## 📈 Results

| Model | Mean Absolute Error | Accuracy |
|-------|-------------------|----------|
| Holt Winters | 14.18 | 86% |
| FB Prophet | 9.32 | 91% |
| LSTM | 8.39 | 92% |

**Average Combined Accuracy**: 90%

## 🚀 Installation & Setup

### Prerequisites
- Python 3.8+
- pip package manager

### Installation Steps

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/electrical-load-forecasting.git
cd electrical-load-forecasting
```

2. **Create virtual environment**
```
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**
```
pip install -r requirements.txt
```

4. **Prepare your data**
- Place your electricity consumption data in data/ directory
- Ensure data includes timestamp and consumption columns\

5. **Train models**
```
python train_models.py
```

6. **Run the web application**
```
python app.py
```

##  Project Structure

```
electrical-load-forecasting/
│
├── data/                    # Dataset files
├── notebooks/              # Jupyter notebooks for exploration
├── src/
│   ├── preprocessing.py    # Data preprocessing functions
│   ├── holt_winters.py    # Holt-Winters implementation
│   ├── prophet_model.py   # FB Prophet implementation
│   ├── lstm_model.py      # LSTM neural network
│   ├── evaluation.py      # Model evaluation metrics
│   └── utils.py           # Utility functions
│
├── models/                 # Trained model files
├── static/                # Web app static files
├── templates/             # HTML templates
├── app.py                 # Flask application
├── train_models.py        # Training script
├── requirements.txt       # Python dependencies
└── README.md              # This file
```

## Requirements

Key dependencies include:

- pandas

- numpy

- scikit-learn

- tensorflow/keras

- prophet

- statsmodels

- flask

- matplotlib

- seaborn

## Usage

### Through Web Interface

- Start the application:
```
bash
python app.py
```

- Open browser and navigate to http://localhost:5000

- Select a date using the date picker

- Click "Forecast" to get predictions from all three models

- View results and visualizations

### Through Python API

```
from src.holt_winters import HoltWintersForecaster
from src.prophet_model import ProphetForecaster
from src.lstm_model import LSTMForecaster

# Initialize models
hw = HoltWintersForecaster()
prophet = ProphetForecaster()
lstm = LSTMForecaster()

# Make predictions
hw_pred = hw.predict(date='2023-12-25')
prophet_pred = prophet.predict(date='2023-12-25')
lstm_pred = lstm.predict(date='2023-12-25')
```

## Methodology

### Data Preprocessing

- Time-series decomposition

- Handling missing values

- Feature extraction (hour, day, month, year, weekday, etc.)

- Normalization and scaling

### Model Training

- Holt-Winters: Optimized seasonal parameters

- Prophet: Custom seasonality and holiday effects

- LSTM: Sequence modeling with attention to temporal patterns

### Evaluation Metrics

- Mean Absolute Error (MAE)

- Root Mean Square Error (RMSE)

- Mean Absolute Percentage Error (MAPE)

- R-squared Score

## Research Background

Based on the research paper "Electrical Load Forecasting" published in the International Journal of Creative Research Thoughts (IJCRT), this project addresses the critical need for accurate electricity demand forecasting in modern power systems. The research highlights the complexity of demand patterns due to energy market deregulation and the importance of customized forecasting approaches for different electrical networks.
