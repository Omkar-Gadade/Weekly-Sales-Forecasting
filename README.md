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
├── data/
├── Final_Models (pkl_files)/
├── Forecast output (csv_files)/
├── eda_notebook.ipynb
├── forecasting_modeling.ipynb
├── requirements.txt
└── README.md
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








