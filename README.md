# Sales Forecasting & Business Intelligence Dashboard

## 📌 Project Overview

**Sales Forecasting & Business Intelligence Dashboard** is an end-to-end data analytics and machine learning project focused on analyzing historical retail sales, identifying sales trends and patterns, building forecasting models, and generating future sales predictions.

The project combines **Python, Pandas, NumPy, Scikit-learn, Matplotlib, and Power BI** to transform raw sales data into meaningful business insights and forecasts.

The main objective is to help businesses understand historical sales performance and estimate future sales to support data-driven planning and decision-making.

---

## 🎯 Objectives

* Analyze historical sales performance.
* Clean and prepare the sales dataset.
* Perform exploratory data analysis (EDA).
* Identify sales trends and seasonal patterns.
* Analyze store and department performance.
* Create time-series forecasting features.
* Compare different machine-learning approaches.
* Evaluate forecasting performance.
* Generate a 12-week future sales forecast.
* Build an interactive Business Intelligence dashboard using Power BI.

---

## 🛠️ Technologies Used

| Technology       | Purpose                                     |
| ---------------- | ------------------------------------------- |
| Python           | Data analysis and forecasting               |
| Pandas           | Data cleaning and transformation            |
| NumPy            | Numerical calculations                      |
| Matplotlib       | Data visualization                          |
| Scikit-learn     | Machine learning                            |
| Jupyter Notebook | Development and analysis                    |
| Power BI         | Interactive business intelligence dashboard |
| Git & GitHub     | Version control and project hosting         |

---

## 📂 Project Structure

```text
Sales-Forecasting-Business-Intelligence-Dashboard/
│
├── data/
│   ├── raw/
│   │   ├── train.csv
│   │   ├── features.csv
│   │   └── stores.csv
│   │
│   └── processed/
│       └── sales_cleaned.csv
│
├── notebooks/
│   ├── 01_Data_Loading_and_Inspection.ipynb
│   ├── 02_EDA_and_Data_Preprocessing.ipynb
│   └── 03_Sales_Forecasting.ipynb
│
├── outputs/
│   ├── charts/
│   │   ├── 01_monthly_sales_trend.png
│   │   ├── 09_weekly_total_sales_trend.png
│   │   ├── 10_actual_vs_forecast.png
│   │   ├── 11_feature_importance.png
│   │   └── 12_future_sales_forecast.png
│   │
│   └── future_sales_forecast.csv
│
├── powerbi/
│   └── Sales_Forecasting_BI_Dashboard.pbix
│
├── requirements.txt
├── .gitignore
└── README.md
```

> Update the filenames above if your actual notebook or Power BI filenames are different.

---

## 📊 Dataset

The project uses historical retail sales data containing information such as:

* Store
* Department
* Date
* Weekly Sales
* Holiday indicator
* Temperature
* Fuel Price
* CPI
* Unemployment
* Store Type
* Store Size

The original data was combined into a single analytical dataset containing:

**421,570 records and 21 columns**

After aggregation by date, the project contains:

**143 weekly sales observations**

---

## 🔄 Project Workflow

```text
Raw Dataset
     │
     ▼
Data Loading
     │
     ▼
Data Cleaning & Validation
     │
     ▼
Exploratory Data Analysis
     │
     ▼
Feature Engineering
     │
     ▼
Weekly Sales Aggregation
     │
     ▼
Forecasting Feature Creation
     │
     ▼
Train/Test Split
     │
     ▼
Forecasting Models
     │
     ├── Baseline
     ├── Linear Regression
     └── Random Forest
     │
     ▼
Model Evaluation
     │
     ▼
12-Week Future Forecast
     │
     ▼
Power BI Dashboard
     │
     ▼
Business Insights
```

---

# 🔍 Exploratory Data Analysis

The project analyzes:

* Overall sales trends
* Monthly sales patterns
* Store performance
* Department performance
* Holiday vs non-holiday sales
* Store type performance
* Weekly sales trends
* Sales distribution
* Correlations between numerical variables

The historical weekly sales analysis contains **143 weeks** of data.

The average total sales across a week were approximately **$47.11 million** after aggregating sales across stores and departments.

---

# 🤖 Sales Forecasting

To prepare the data for forecasting, several time-based features were created.

### Lag Features

* Lag 1 week
* Lag 2 weeks
* Lag 4 weeks
* Lag 8 weeks
* Lag 12 weeks

### Rolling Features

* 4-week rolling average
* 8-week rolling average
* 12-week rolling average

### Calendar Features

* Year
* Month
* Quarter
* Week number

The final test period consisted of the last **12 historical weeks**, while the earlier observations were used for training.

---

# 📈 Model Evaluation

Three approaches were evaluated on the 12-week test period:

| Model             |     MAE |    RMSE |  MAPE |
| ----------------- | ------: | ------: | ----: |
| Baseline          | $1.103M | $1.748M | 2.40% |
| Linear Regression | $2.150M | $2.725M | 4.77% |
| Random Forest     | $1.029M | $1.245M | 2.24% |

The Random Forest model produced the lowest error values among the tested models on this particular 12-week holdout period.

### Evaluation Metrics

**MAE — Mean Absolute Error**

Measures the average absolute difference between actual and predicted sales.

**RMSE — Root Mean Squared Error**

Penalizes larger prediction errors more heavily.

**MAPE — Mean Absolute Percentage Error**

Expresses prediction error as a percentage of actual sales.

---

# 🔮 Future Sales Forecast

The Random Forest model was used to generate a **12-week future sales forecast** beyond the historical dataset.

### Forecast Summary

* **Forecast period:** 12 weeks
* **Total forecasted sales:** $625.82 million
* **Average forecasted weekly sales:** $52.15 million
* **Highest forecast:** approximately $65.71 million
* **Lowest forecast:** approximately $44.17 million

The forecast results are stored in:

```text
outputs/future_sales_forecast.csv
```

---

# 📊 Business Intelligence Dashboard

The Power BI dashboard is designed to provide an interactive overview of sales performance.

### Planned Dashboard Components

* Total Historical Sales
* Average Weekly Sales
* Total Stores
* Total Departments
* Historical Weekly Sales Trend
* Sales by Store
* Sales by Department
* Holiday vs Non-Holiday Sales
* Sales by Store Type
* Monthly Sales
* Historical vs Forecasted Sales

The dashboard allows users to explore sales performance through interactive filters and visualizations.

---

# 💡 Key Insights

Some important findings from the analysis include:

1. Historical sales show clear weekly variation.
2. Significant sales spikes occur around certain holiday periods.
3. Previous-week and previous-period sales features contribute strongly to the forecasting model.
4. The week-of-year feature had the highest Random Forest feature importance in the tested model.
5. The final forecasting model provides a 12-week projection for future planning.
6. Store and department-level analysis can be used to identify differences in sales performance.

> Feature importance indicates how much a model uses a feature for prediction; it should not be interpreted as proof that the feature causes sales changes.

---

# 📁 Important Output Files

### Processed Dataset

```text
data/processed/sales_cleaned.csv
```

### Future Forecast

```text
outputs/future_sales_forecast.csv
```

### Forecast Charts

```text
outputs/charts/
```

### Power BI Dashboard

```text
powerbi/Sales_Forecasting_BI_Dashboard.pbix
```

---

# 🚀 How to Run the Project

## 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/Sales-Forecasting-Business-Intelligence-Dashboard.git
```

## 2. Navigate to the project

```bash
cd Sales-Forecasting-Business-Intelligence-Dashboard
```

## 3. Create a virtual environment

```bash
python -m venv sales_forecasting_env
```

## 4. Activate the environment

### Windows

```bash
sales_forecasting_env\Scripts\activate
```

> Note: The correct folder is `Scripts`, not `Scriplts`.

## 5. Install dependencies

```bash
pip install -r requirements.txt
```

## 6. Start Jupyter Notebook

```bash
jupyter notebook
```

Open the notebooks inside the `notebooks` folder and execute them in order.

---

# 📦 Requirements

The main Python libraries used are:

```text
pandas
numpy
matplotlib
scikit-learn
jupyter
```

---

# 👨‍💻 Author

**Jakka Syam Babu**

B.Tech — Computer Science and Data Science

---

# ⭐ Project Highlights

* End-to-end data analytics project
* 421K+ historical records analyzed
* 143 weekly observations created
* Exploratory Data Analysis
* Time-series feature engineering
* Machine-learning forecasting
* Model comparison using MAE, RMSE and MAPE
* 12-week future sales forecast
* Power BI Business Intelligence dashboard
* GitHub version-controlled project
