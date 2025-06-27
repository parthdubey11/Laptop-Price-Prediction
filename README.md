# Laptop-Price-Prediction
This project is a **machine learning-based regression system** that predicts the price of a laptop based on its specifications. It leverages Python libraries like **scikit-learn**, **pandas**, **NumPy**, and **Streamlit** for building the model and creating an interactive user interface.

---

## 📌 Problem Statement

Many users find it difficult to estimate a fair price for a laptop based on its hardware features. This project solves that problem by predicting a laptop’s price using trained ML models on historical laptop specification data.

---

## 🛠️ Features & Specs Used

The model considers the following specifications to predict the laptop's price:

- Company (Brand)
- Type (Notebook, Ultrabook, etc.)
- RAM (in GB)
- Weight (in kg)
- Touchscreen (Yes/No)
- IPS Display (Yes/No)
- Screen Size (in inches)
- Screen Resolution (used to calculate PPI)
- CPU Brand
- HDD Size
- SSD Size
- GPU Brand
- Operating System

---

## 📂 Dataset

- The dataset (`laptop_data.csv`) was cleaned and processed:
  - Removed units like "GB", "kg", "GHz" from values
  - Extracted CPU and GPU brands
  - Computed **Pixels Per Inch (PPI)** from screen size and resolution
  - Split and converted memory columns to numeric types
  - Handled mixed storage types (e.g. 128GB SSD + 1TB HDD)

---

## 🧠 Model

- Several regressors were trained and evaluated:
  - **Linear Regression**
  - **Ridge Regression**
  - **Lasso Regression**
  - **XGBoost Regressor**
  - **Stacking Regressor** (used in production)

- Final pipeline:
  - Preprocessing: OneHotEncoding + StandardScaler
  - Model: **Stacked Ensemble** with best-performing base models

---

## 🚀 Web App

The project is deployed via **Streamlit** with a user-friendly interface to:

1. Input laptop specs through dropdowns/sliders
2. Predict the price with a click
3. Display the predicted price dynamically

To run the app:
```bash
streamlit run app.py
