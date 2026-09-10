# Healthcare Readmission Risk Analytics

End-to-end healthcare analytics project predicting 30-day hospital readmissions using 100K+ hospital encounters. The project covers data cleaning, exploratory analysis, statistical testing, machine learning model comparison, and SHAP-based model interpretation.

## Project Overview

- **Dataset:** Diabetes 130-US Hospitals for Years 1999–2008 (UCI)
- **Records:** 101,766 hospital encounters
- **Target:** 30-day hospital readmission
- **Task:** Binary classification

## Workflow

1. Data cleaning with Pandas
2. Exploratory Data Analysis with Pandas, NumPy and Matplotlib
3. Statistical hypothesis testing using SciPy
4. Machine learning model development
5. Model evaluation using Precision, Recall, F1-score and ROC-AUC
6. Feature importance analysis
7. SHAP-based model interpretation

## Machine Learning Models

- Logistic Regression
- Decision Tree
- Random Forest

## Model Performance

| Model | Precision | Recall | F1-Score | ROC-AUC |
|---|---:|---:|---:|---:|
| **Decision Tree** | 17.39% | **60.63%** | **27.03%** | **0.662** |
| Random Forest | **18.76%** | 46.98% | 26.81% | **0.660** |
| Logistic Regression | 17.28% | 52.18% | 25.97% | 0.647 |

The Decision Tree achieved the highest Recall, F1-score and ROC-AUC among the evaluated models.

## Exploratory Data Analysis

### 30-Day Readmission Distribution

![Readmission Distribution](visualizations/eda/readmission_distribution.png)

### Readmission Rate by Age

![Readmission by Age](visualizations/eda/readmission_by_age.png)

### Readmission Rate by Length of Stay

![Readmission by Stay](visualizations/eda/readmission_by_stay.png)

### Readmission Rate by Prior Inpatient Visits

![Readmission by Inpatient Visits](visualizations/eda/readmission_by_inpatient.png)

### Readmission Rate by Number of Medications

![Readmission by Medications](visualizations/eda/readmission_by_medications.png)

## Model Interpretation

### SHAP Feature Importance

![SHAP Feature Importance](visualizations/modelling/shap_summary.png)

The most influential features included prior inpatient visits, discharge disposition, number of diagnoses, length of hospital stay, number of medications, insulin status and prior emergency visits.

## Key Findings

- 30-day readmissions represented **11.16%** of encounters.
- Prior inpatient utilization was the strongest SHAP feature.
- Patient complexity and healthcare utilization were important predictive factors.
- The Decision Tree achieved the highest recall at **60.63%**, making it the strongest model for identifying potential readmissions in this evaluation.

## Repository Structure

```text
Healthcare-Readmission-Risk-Analytics/
│
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_eda.ipynb
│   ├── 03_statistical_analysis.ipynb
│   └── 04_modeling.ipynb
│
├── visualizations/
│   ├── eda/
│   └── modeling/
│
├── data/
│   └── (excluded from GitHub)
│
├── requirements.txt
├── .gitignore
└── README.md
````

## Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* SciPy
* Scikit-learn
* SHAP
* Jupyter Notebook

## Data

The dataset is not included in this repository.

Download the **Diabetes 130-US Hospitals for Years 1999–2008** dataset from the UCI Machine Learning Repository and place the files inside `data/raw/`.

Processed datasets and analysis outputs are also excluded from GitHub.

## Disclaimer

This project is intended for analytical and educational purposes. Model predictions should not be interpreted as clinical decisions.



**One thing:** make sure the actual `.png` files are committed under `visualizations/`, otherwise GitHub will show broken images.
```
