# 📱 Mobile Price Prediction using Machine Learning

## 📌 Overview

This project predicts the price category of mobile phones using Machine Learning classification algorithms. The objective is to classify a mobile device into one of four price ranges based on its hardware specifications.

---

## 📂 Dataset

- Training Samples: 2000
- Test Samples: 1000
- Features: 20
- Target Variable: `price_range`

---

## 🔄 Workflow

1. Data Understanding
2. Data Cleaning
3. Exploratory Data Analysis (EDA)
4. Correlation Analysis
5. Data Preprocessing
6. Model Comparison
7. Hyperparameter Tuning
8. Feature Engineering
9. Feature Selection (RFE)
10. Final Prediction

---

## 🤖 Models Evaluated

- Logistic Regression
- Decision Tree
- Random Forest
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)
- Gaussian Naive Bayes
- XGBoost

---

## 🏆 Final Model

- Logistic Regression
- Recursive Feature Elimination (RFE)
- StandardScaler

Selected Features:

- Battery Power
- Mobile Weight
- Pixel Height
- Pixel Width
- RAM

---

## 📊 Performance

| Metric | Score |
|--------|-------|
| Training Accuracy | **97.90%** |
| Cross Validation Accuracy | **97.19%** |
| Test Accuracy | **98.75%** |

---

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost

---

## 📁 Project Structure

```
Mobile_Price_Prediction/
│
├── notebook.ipynb
├── train.csv
├── test.csv
├── submission.csv
├── README.md
└── requirements.txt
```

---

## 👩‍💻 Author

Lavina Fand