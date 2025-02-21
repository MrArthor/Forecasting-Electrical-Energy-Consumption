# Forecasting Electrical Energy Consumption

This repository hosts a Streamlit-based web application for forecasting electrical energy consumption. The project leverages a suite of time series analysis techniques—including ARIMA, SARIMA, and TBATS models—to process, analyze, and forecast power consumption. In addition, the repository features interactive visualizations, statistical tests (ADF & KPSS), and an embedded BI dashboard for deeper insights.

## Overview

The application is designed to:

- **Load & Preprocess Data:** Read raw electrical energy data from a CSV file, perform date parsing, and compute aggregate power consumption. Various transformations (e.g., Box-Cox and Yeo-Johnson) are applied to reduce skewness and prepare the data for forecasting citeturn0file0.
- **Data Visualization:** Generate interactive plots including box plots, distribution histograms, time series charts, and correlograms using Plotly, Seaborn, and Matplotlib.
- **Outlier Detection & Statistical Analysis:** Identify outliers in total power consumption and perform stationarity tests (ADF and KPSS) to assess if differencing is needed.
- **Forecasting Models:** Build and evaluate multiple forecasting models (ARIMA, SARIMA, TBATS), save trained models for reproducibility, and compare their performance using metrics such as MSE, MAE, RMSE, and R².
- **Business Intelligence:** Embed a Power BI dashboard to offer additional visual insights.

## Repository Structure

The repository is organized as follows:

```
Bi DashBoard/         # Contains files and assets for the embedded business intelligence dashboard.
DataSet/              # Contains the dataset (e.g., expanded_dataset.csv) used for forecasting.
Implementation/       # Contains the main application source code (e.g., WebPage_Backup.py) and related scripts.
Report/               # Contains project reports, documentation, and supplementary analysis.
.gitattributes        # Git configuration file.
.gitignore            # Specifies intentionally untracked files to ignore.
requirements.txt      # List of Python dependencies required to run the application.
README.md             # This file.
```

## Setup & Installation

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/MrArthor/Forecasting-Electrical-Energy-Consumption.git
   cd Forecasting-Electrical-Energy-Consumption
   ```

2. **Create and Activate a Virtual Environment (recommended):**

   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

   *Key dependencies include:*  
   - streamlit  
   - pandas  
   - numpy  
   - matplotlib  
   - seaborn  
   - scikit-learn  
   - statsmodels  
   - pmdarima  
   - tbats  
   - plotly

4. **Dataset Placement:**

   Place the dataset file (e.g., `expanded_dataset.csv`) inside the `DataSet` folder. Ensure that file paths in the code are updated if necessary.

## Running the Application

Launch the Streamlit application by running:

```bash
streamlit run Implementation/API_Deployment/WebPage_Backup.py
```

This command opens the interactive dashboard in your default web browser. Use the sidebar menu to navigate between different pages such as data visualizations, forecasting models, and the BI dashboard.

## Usage

- **HOME:** Provides an introduction with a brief overview and an introductory video.
- **Box Plots & Data Distribution:** Visualize raw and transformed data to understand distributions and detect outliers.
- **Time Series Analysis:** Analyze trends, and seasonal patterns, and perform stationarity testing.
- **Forecasting Models:** Train and evaluate ARIMA, SARIMA, and TBATS models. View residuals, metrics, and forecasts compared to actual values.
- **BI Dashboard:** Access an embedded Power BI dashboard for advanced business insights.

## Contributing

Contributions are welcome! If you have improvements, bug fixes, or additional features to suggest, please open an issue or submit a pull request.
