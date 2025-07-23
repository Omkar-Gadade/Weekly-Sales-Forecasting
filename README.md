# 📊 Weekly Sales Forecasting - Data Science Assignment

## 📁 Project Overview

This project builds a forecasting model to predict weekly sales quantities for a set of products over the next 3 months (Sep, Oct, Nov 2024), using historical weekly sales data.

---

## 📌 Tasks Covered

- Exploratory Data Analysis (EDA)
- Time Series Forecasting (using Prophet)
- Validation on June–August 2024
- Final Forecast Generation for Sep–Nov 2024

---

## 🗂 Folder Structure

```
Weekly-Sales-Forecasting/
│
├── data/
│   └── Assessment-2-Associate-DS(in).csv                # Raw input dataset
│
├── Final_Models (pkl_files)/
│   ├── prophet_bestmodel_Serial_no1.pkl                # Trained Prophet model for Serial No. 1
│   ├── prophet_bestmodel_Serial_no2.pkl                # Trained Prophet model for Serial No. 2
│   ├── prophet_bestmodel_Serial_no3.pkl                # Trained Prophet model for Serial No. 3
│   ├── prophet_bestmodel_Serial_no4.pkl                # Trained Prophet model for Serial No. 4
│   └── prophet_bestmodel_Serial_no5.pkl                # Trained Prophet model for Serial No. 5
│
├── Forecast output (csv_files)/
│   ├── forecast_sep_oct_nov_2024_Model_Serial_No_1.csv  # Forecasted sales for Serial No. 1 (Sep-Nov 2024)
│   ├── forecast_sep_oct_nov_2024_Model_Serial_No_2.csv  # Forecasted sales for Serial No. 2 (Sep-Nov 2024)
│   ├── forecast_sep_oct_nov_2024_Model_Serial_No_3.csv  # Forecasted sales for Serial No. 3 (Sep-Nov 2024)
│   ├── forecast_sep_oct_nov_2024_Model_Serial_No_4.csv  # Forecasted sales for Serial No. 4 (Sep-Nov 2024)
│   └── forecast_sep_oct_nov_2024_Model_Serial_No_5.csv  # Forecasted sales for Serial No. 5 (Sep-Nov 2024)
│
├── venv/                                               # Virtual environment
│
├── eda_notebook.ipynb                                  # Exploratory Data Analysis notebook
├── forecasting_modeling.ipynb                          # Main modeling and forecasting notebook
│
├── requirements.txt                                    # List of required Python packages
├── LICENSE
└── README.md                                           # This file

```



---

## 📈 Forecasting Models Used

- `Prophet` – time series modeling


---

## 🧪 Validation Metric

**Monthly Accuracy** is calculated using:

$$
\text{Monthly Accuracy} = 1 - \frac{\sum |\hat{y} - y|}{\sum y}
$$


---

## 🔍 Model Details

- Models used: **Facebook Prophet**
- Trained on data till: **June 2024**
- Validation period: **June 2024 – August 2024**
- Forecasting period: **September 2024 – November 2024**
- Each `.pkl` model corresponds to a unique product (`SerialNum`)
- These models can be used to make further forecasts using Prophet’s `predict()` method

---

## 📤 Forecast Output

- Output forecasts are stored as `.csv` files inside the `Forecast output (csv_files)` directory
- Each file contains forecasted weekly sales from **September to November 2024** for each product (Serial Number)

---

## 🔁 Reproducibility

To recreate this project:

```bash
# Clone repo
git clone https://github.com/Omkar-Gadade/Weekly-Sales-Forecasting.git
cd Weekly-Sales-Forecasting

# Create virtual environment 
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows

# Install dependencies
pip install -r requirements.txt

----------------------------------------------------------------------
# Load any saved model from the Final_Models directory:

import joblib
model = joblib.load('Final_Models/prophet_bestmodel_Serial_no1.pkl')

# Use the model to predict future sales:

future = model.make_future_dataframe(periods=13, freq='W')
forecast = model.predict(future)

```








