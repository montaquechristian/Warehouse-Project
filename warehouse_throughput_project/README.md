# Warehouse Throughput Prediction

A small Industrial Engineering / machine learning portfolio project that predicts hourly warehouse throughput from operational conditions.

## Project Summary

The project uses a **synthetic warehouse operations dataset** with 3,000 hourly observations. The dataset includes:

- Staffing level
- Order volume
- Average items per order
- Average pick distance
- Automation utilization
- Absenteeism
- Equipment downtime
- New-hire share
- Shift
- Day of week
- Peak-period indicator

The target variable is **throughput in units per hour**.

> **Important:** The dataset is simulated for portfolio use. It does not contain Amazon data or any proprietary employer information.

## Tools

- Python
- pandas
- NumPy
- scikit-learn
- matplotlib
- Jupyter Notebook

## Machine Learning Models

The notebook compares:

1. Linear Regression
2. Random Forest Regression
3. Gradient Boosting Regression

### Test-set results

| Model             |   MAE |   RMSE |    R2 |
|:------------------|------:|-------:|------:|
| Linear Regression | 6.215 |  7.768 | 0.828 |
| Gradient Boosting | 6.627 |  8.257 | 0.805 |
| Random Forest     | 7.035 |  8.991 | 0.769 |

**Best model:** Linear Regression

## Key Findings

- Best-model MAE: **6.22 units/hour**
- Best-model RMSE: **7.77 units/hour**
- Best-model R²: **0.828**
- Most influential variables in this run: **staff_count, order_volume, equipment_downtime_min, shift, automation_utilization_pct**

These results show how warehouse operational data can be translated into a predictive model that supports capacity planning and process analysis.

## Project Structure

```text
warehouse_throughput_project/
├── warehouse_throughput_prediction.ipynb
├── warehouse_operations_synthetic.csv
├── model_metrics.csv
├── feature_importance.csv
├── requirements.txt
├── README.md
├── RESUME_BULLETS.md
└── charts/
    ├── predicted_vs_actual.png
    ├── feature_importance.png
    └── throughput_by_shift.png
```
