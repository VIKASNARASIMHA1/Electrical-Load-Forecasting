# Changelog: Electrical Load Forecasting

All notable changes to this project are documented here.

The project has not yet followed formal version tagging.

**Note**: The project was developed as a continuous engineering effort based on research published in IJCRT. Formal semantic versioning begins from v0.1.0.

## [0.1.0] - 2026-01-10

### Added
- Complete implementation of three forecasting models:
  - **Holt-Winters Exponential Smoothing** with optimized seasonal parameters (86% accuracy)
  - **Facebook Prophet** with custom seasonality and holiday effects (91% accuracy)
  - **LSTM Neural Network** with three-gate architecture (92% accuracy)
- Unified data preprocessing pipeline with:
  - Time-series decomposition
  - Missing value handling and outlier detection
  - Temporal feature extraction (hour, day, month, year, weekday)
  - Normalization and scaling functions
- Feature engineering module creating rich temporal features for all models
- Comprehensive evaluation framework with four metrics:
  - Mean Absolute Error (MAE)
  - Root Mean Square Error (RMSE)
  - Mean Absolute Percentage Error (MAPE)
  - R-squared Score
- Flask web application with:
  - HTML/CSS frontend interface
  - Date picker for forecast selection
  - Real-time predictions from all three models
  - Comparative visualization of results
  - ngrok tunneling support for temporary public access
- Modular project structure with clear separation of concerns:
  - `src/preprocessing.py`: Data cleaning and feature engineering
  - `src/holt_winters.py`: Statistical forecasting implementation
  - `src/prophet_model.py`: Bayesian structural time series
  - `src/lstm_model.py`: Deep learning architecture
  - `src/evaluation.py`: Metric calculations and model comparison
  - `src/utils.py`: Shared utility functions
- Jupyter notebooks for exploratory analysis and model development
- Model serialization and persistence in `models/` directory
- Static assets and HTML templates for web interface
- Training script (`train_models.py`) for end-to-end model training
- Requirements.txt with all dependencies (pandas, numpy, scikit-learn, tensorflow, prophet, statsmodels, flask, matplotlib, seaborn)
- Research paper (IJCRT2207165.pdf) documenting methodology and findings
- Comprehensive README with installation, usage, and project overview
- MIT License and contribution guidelines

### Performance
- Holt-Winters MAE: 14.18 | Accuracy: 86%
- FB Prophet MAE: 9.32 | Accuracy: 91%
- LSTM MAE: 8.39 | Accuracy: 92%
- Combined average accuracy: 90%
- Training times (CPU):
  - Holt-Winters: <30 seconds
  - Prophet: 2-3 minutes
  - LSTM: 15-20 minutes
- Inference latency: <100ms per prediction
- Web application response: <500ms end-to-end

### Documentation
- Research methodology based on IJCRT publication
- Installation and setup instructions
- Usage examples for both web interface and Python API
- Model comparison results and interpretation
- Project structure overview

### Acknowledgments
- Based on research published in International Journal of Creative Research Thoughts (IJCRT)
- Inspired by classical time-series forecasting literature and modern deep learning advances
- Built with open-source tools and libraries from the Python data science ecosystem
