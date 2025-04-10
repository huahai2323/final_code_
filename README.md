# COVID-19 Patient Survival Prediction (with Streamlit App)

This project builds a machine learning system to predict whether a COVID-19 patient will survive, based on their clinical and demographic information. The system supports both notebook-based exploration and an interactive web interface built with Streamlit.

---

## 📊 Project Overview

- **Problem**: Predict patient survival (Alive/Deceased) from COVID-19 medical record data.
- **Dataset**: Public dataset provided by the Mexican Government (over 1 million records).
- **Target Variable**: `ALIVE` (1 = survived, 0 = deceased).
- **Core Models**:
  - Logistic Regression (with tuning)
  - Random Forest (with tuning)
  - XGBoost (with tuning)
  - Stacking Ensemble (LR + RF → XGB as meta-learner)

---

## ⚙️ Installation

### 1. Python Environment

- Python version: 3.10+
- Recommended: Use [Anaconda](https://www.anaconda.com/)

### 2. Required Libraries

Install dependencies using:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn xgboost streamlit
```

---

## 🚀 How to Run

### Option A: Jupyter Notebook

1. Open 'Data preprocessing.ipynb'   
2. Run cells sequentially to:
   - Preprocess data
   - Train models
   - Visualize metrics (confusion matrix, ROC, AUC, etc.)

### Option B: Web App via Streamlit

1. Run this command in terminal:

```bash
streamlit run app.py
```

2. Upload `Covid Data.csv` when prompted.
3. App will:
   - Clean and preprocess data
   - Train tuned Stacking model
   - Display Accuracy, F1, AUC
   - Show ROC curve

---

## 📁 File Structure

```
├── app.py                  # Streamlit app entry point
├── Data preprocessing.ipynb# Full model training and tuning code 
├── Covid Data.csv          # Raw dataset (user-provided)
├── covid_subset_*.csv      # Optional mini test datasets (for app testing)
```

---

## 🧠 Acknowledgements

- Part of the data cleaning and feature engineering logic was adapted (with modification) from a public Kaggle notebook authored by **Kaan Karaduman**:  
  https://www.kaggle.com/code/kaanxtr/covid-19-visualization-machine-learning/notebook

- The Streamlit implementation and model tuning pipeline were developed by the project author.

- Supervision and academic guidance provided by **Dr. Isaac Osei Agyemang**.

---

## 📌 Notes

- No proprietary or non-public datasets were used.
- All non-original code has been credited.
- This repository is for academic purposes and should not be used for clinical decisions.