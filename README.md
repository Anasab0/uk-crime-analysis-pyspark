# UK Crime Data Analysis & Loan Prediction — Big Data & ML Project

A big data analytics and machine learning project built with Apache Spark (PySpark), 
analysing 578,000+ UK police crime records and building a loan prediction 
classification pipeline.

---

## Overview

This project is split into two parts:

**Part A — UK Crime Data Analysis (Apache Spark)**  
Exploratory and descriptive analysis of real UK police crime data across three 
counties: Derbyshire, Leicestershire, and Nottinghamshire (2023–2024).

**Part B — Loan Prediction (MLlib Classification)**  
A full machine learning pipeline predicting loan approval outcomes using three 
classification algorithms.

---

## Part A — Crime Data Analysis

### Dataset
- Source: UK Police open crime data
- Records: 578,000+ crime incidents
- Counties: Derbyshire, Leicestershire, Nottinghamshire
- Period: January 2023 – December 2024

### What I Did
- Loaded and preprocessed multi-county CSV data using PySpark
- Standardised county names and removed duplicates
- Performed Spark SQL queries for descriptive analysis
- Identified monthly crime trends, peak crime months, and crime type distributions

### Key Findings
- Nottinghamshire had the highest total crimes (202,628), followed by 
  Leicestershire (198,266) and Derbyshire (177,265)
- Violence and sexual offences was the most common crime type across all three counties
- Crime peaked in May/June across counties and dropped in winter months

### Visualisations
- Line chart: Monthly crime trends per county (2023–2024)
- Bar chart: Crime type distribution across counties
- Pie charts: Crime type breakdown per county

---

## Part B — Loan Prediction

### Dataset
- Loan application records with applicant demographics and financial features
- Features: Gender, Marital Status, Education, Income, Loan Amount, Credit History, 
  Property Area

### ML Pipeline
1. Missing value removal
2. Categorical encoding (StringIndexer + OneHotEncoder)
3. Feature assembly (VectorAssembler)
4. Train/test split (72/28)
5. Model training and evaluation

### Models & Results

| Model               | Accuracy | Precision | Recall |
|---------------------|----------|-----------|--------|
| Logistic Regression | 76.8%    | 76.3%     | 76.8%  |
| Decision Tree       | 75.0%    | 73.9%     | 75.0%  |
| Naive Bayes         | 55.4%    | 61.3%     | 55.4%  |

Logistic Regression outperformed both other models across all metrics.

---

## Technologies Used

- Python
- Apache Spark (PySpark)
- Spark SQL
- PySpark MLlib
- Pandas
- Matplotlib
- Seaborn
- Kaggle Notebooks

---

## How to Run

1. Open the notebook on Kaggle: (https://www.kaggle.com/code/anasabjaou/coursework)
2. Ensure the crime dataset and loan dataset are attached under the Input section
3. Run all cells in order — Part A first, then Part B

Or clone locally:
```bash
git clone https://github.com/yourusername/uk-crime-analysis-pyspark
cd uk-crime-analysis-pyspark
pip install pyspark pandas matplotlib seaborn
jupyter notebook
```

---

## Author

Anas Abjaou  
[LinkedIn](https://www.linkedin.com/in/anas-abjaou) | 
[GitHub](https://github.com/Anasab0)
