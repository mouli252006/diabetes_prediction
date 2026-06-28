
# Diabetes Prediction System

A machine learning application designed to predict the likelihood of a patient having diabetes based on specific clinical measurements. This system uses classification algorithms to analyze medical data and provide an early risk assessment.

## How it Works

The application processes clinical data through a structured machine learning pipeline:

1. **Data Preprocessing & Cleaning:** Handles missing or invalid zero values in clinical indicators (like Glucose, Insulin, and Blood Pressure) using median imputation.
2. **Feature Scaling:** Normalizes numerical features using StandardScaler so that high-magnitude values (like Insulin) don't dominate variables with smaller ranges (like Age).
3. **Classification Model:** Trains on the dataset using algorithms like Logistic Regression, Support Vector Machines (SVM), or Random Forest to find the optimal boundary between diabetic and non-diabetic profiles.

## Health Predictors Evaluated

The system makes predictions based on the following patient metrics:

* **Glucose:** Plasma glucose concentration (2 hours in an oral glucose tolerance test).
* **BloodPressure:** Diastolic blood pressure (mm Hg).
* **SkinThickness:** Triceps skin fold thickness (mm).
* **Insulin:** 2-Hour serum insulin (mu U/ml).
* **BMI:** Body Mass Index ($weight\ in\ kg / (height\ in\ m)^2$).
* **DiabetesPedigreeFunction:** A score that scores genetic family history risk.
* **Age & Pregnancies:** Age in years and the number of pregnancies.

## Features

* **Clinical Data Pipeline:** Clean handling of skewed data distributions and missing medical entries.
* **Optimized Classifiers:** Trained to balance precision and recall to minimize dangerous false negatives.
* **Interactive Frontend:** Built with Streamlit, allowing users or healthcare workers to input vitals via sliders/inputs and get instant risk predictions.

## Tech Stack

* **Language:** Python
* **Data & ML:** Pandas, NumPy, Scikit-learn (StandardScaler, Classification Models)
* **Frontend:** Streamlit

## Quick Start

1. **Clone the Repo**
```bash
git clone https://github.com/your-username/diabetic-prediction-system.git
cd diabetic-prediction-system

```


2. **Install Requirements**
```bash
pip install -r requirements.txt

```


3. **Run the Application**
```bash
streamlit run app.py

```



## Repository Structure

* `data/` — Contains the raw and preprocessed medical datasets (e.g., Pima Indians dataset).
* `notebooks/` — Exploratory Data Analysis (EDA), outlier detection, and model benchmarking.
* `models/` — Exported scaler object and trained classification model (`.pkl` files).
* `app.py` — Streamlit web interface script.
