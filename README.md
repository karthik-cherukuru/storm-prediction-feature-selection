# 🌩️ Storm Formation Analysis using Feature Selection

## 📌 Overview

This project focuses on identifying the most influential meteorological factors responsible for storm formation using real-world data from NASA POWER.

The study applies **filter and wrapper feature selection techniques** to determine key variables such as humidity, pressure, and wind, followed by training multiple machine learning models to predict storm events.

---

## 🎯 Objectives

* Analyze meteorological data for storm patterns
* Identify key influencing variables using feature selection
* Compare multiple machine learning models
* Evaluate performance using appropriate metrics

---

## 📂 Project Structure

```
├── 01_data_preparation.ipynb
├── 02_exploratory_data_analysis.ipynb
├── 03_feature_selection.ipynb
├── 04_model_training_evaluation.ipynb
├── data/
│   └── prepared.csv
│   └── data.csv
├── report/
│   └── final_report.pdf
└── README.md
```

---

## 🧪 Dataset

* Source: NASA POWER API
* Location: Visakhapatnam (India)
* Duration: 2014 – 2024
* Frequency: Hourly

### Features Used:

* Temperature
* Dew Point
* Wet Bulb Temperature
* Relative Humidity
* Specific Humidity
* Surface Pressure
* Wind Speed & Direction
* Precipitation

---

## ⚙️ Methodology

### 1️⃣ Data Preparation

* Removed metadata rows
* Handled missing values (-999)
* Created datetime column
* Defined storm threshold using **90th percentile precipitation**

---

### 2️⃣ Exploratory Data Analysis

* Distribution plots
* Storm vs Non-storm comparisons
* Time series analysis
* Monthly storm trends

---

### 3️⃣ Feature Selection

#### 🔍 Filter Methods:

* Correlation Analysis
* Mutual Information
* Variance Threshold

#### 🔁 Wrapper Methods:

* Recursive Feature Elimination (RFE)
* Forward Feature Selection

### ✅ Key Features Identified:

* Specific Humidity
* Dew Point
* Relative Humidity
* Surface Pressure
* Wet Bulb Temperature
* Wind Speed

---

### 4️⃣ Model Training

Models used:

* Logistic Regression
* Decision Tree
* Random Forest
* Gradient Boosting

---

## 📊 Results

| Model               | Accuracy | Precision | Recall | F1 Score | ROC-AUC  |
| ------------------- | -------- | --------- | ------ | -------- | -------- |
| Random Forest       | 0.91     | 0.64      | 0.30   | **0.41** | **0.89** |
| Decision Tree       | 0.87     | 0.37      | 0.40   | 0.38     | 0.66     |
| Gradient Boosting   | 0.90     | 0.64      | 0.21   | 0.32     | 0.87     |
| Logistic Regression | 0.90     | 0.72      | 0.10   | 0.17     | 0.85     |

---

## 🏆 Conclusion

* **Moisture-related variables** (humidity, dew point) are the strongest predictors
* **Low pressure systems** strongly correlate with storm formation
* **Random Forest** performed best overall based on F1-score and ROC-AUC

---

## 🚀 Future Improvements

* Handle class imbalance using SMOTE
* Tune hyperparameters for better recall
* Incorporate additional meteorological variables
* Deploy as a real-time prediction system

---

## 🛠️ Tech Stack

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Scikit-learn

---

## 👨‍💻 Author

Karthik C

---

## ⭐ Acknowledgements

* NASA POWER for providing open meteorological data
* Academic guidance and coursework in Applied Data Science
