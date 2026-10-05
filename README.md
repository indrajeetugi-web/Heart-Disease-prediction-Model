# ❤️ Heart Disease Prediction

A machine learning project that performs exploratory data analysis (EDA) on a heart disease dataset and compares five classification algorithms to predict whether a patient has heart disease. **Logistic Regression** achieved the best accuracy and F1 score.

---

## 📌 Table of Contents
- [Overview](#-overview)
- [Dataset](#-dataset)
- [Project Workflow](#-project-workflow)
- [Models Used](#-models-used)
- [Results](#-results)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)

---

## 🔍 Overview

Heart disease is one of the leading causes of death worldwide. This project explores a clinical dataset to understand which factors relate to heart disease, then trains and compares several classifiers to predict the `HeartDisease` target (1 = disease, 0 = no disease).

## 📊 Dataset

The dataset (`heart.csv`) contains patient records with clinical features such as:

| Feature | Description |
|---|---|
| `Age` | Age of the patient |
| `Sex` | Sex of the patient |
| `ChestPainType` | Type of chest pain |
| `RestingBP` | Resting blood pressure |
| `Cholesterol` | Serum cholesterol |
| `FastingBS` | Fasting blood sugar indicator |
| `RestingECG` | Resting electrocardiogram results |
| `MaxHR` | Maximum heart rate achieved |
| `ExerciseAngina` | Exercise-induced angina |
| `Oldpeak` | ST depression induced by exercise |
| `ST_Slope` | Slope of the peak exercise ST segment |
| `HeartDisease` | **Target** – 1 = heart disease, 0 = normal |


## 🔄 Project Workflow

### 1. Exploratory Data Analysis
- Checked shape, data types, summary statistics, duplicates and missing values
- Plotted the target class distribution
- Visualized distributions of `Age`, `RestingBP`, `Cholesterol` and `MaxHR` using histograms with KDE
- Explored relationships using count plots (chest pain type, fasting blood sugar vs. heart disease), a box plot (cholesterol), a violin plot (age) and a correlation heatmap

### 2. Data Cleaning
- Found invalid zero values in `Cholesterol` and `RestingBP`
- Replaced them with the mean of the valid values (zeros excluded from the cholesterol mean)

### 3. Preprocessing
- One-hot encoded categorical variables (`pd.get_dummies`, `drop_first=True`)
- Standardized numerical columns (`Age`, `RestingBP`, `Cholesterol`, `MaxHR`, `Oldpeak`) with `StandardScaler`
- Split the data 80/20 into train and test sets (`random_state=42`)

### 4. Model Training & Evaluation
Trained five classifiers and compared them using **accuracy** and **F1 score** on the test set.

## 🤖 Models Used

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Naive Bayes (Gaussian)
- Decision Tree
- Support Vector Machine (SVM)

## 🏆 Results

| Model | Accuracy | F1 Score |
|---|---|---|
| **Logistic Regression** | **XX.XX** | **XX.XX** |
| KNN | XX.XX | XX.XX |
| Naive Bayes | XX.XX | XX.XX |
| Decision Tree | XX.XX | XX.XX |
| SVM | XX.XX | XX.XX |

> 🔧 Replace the `XX.XX` placeholders with the values from your notebook's `result` output.

**Logistic Regression** performed best on both metrics, so it was selected as the final model.

## 🛠 Tech Stack

- Python 3
- NumPy, Pandas
- Matplotlib, Seaborn
- Scikit-learn
- Joblib
- Jupyter Notebook


## 📁 Project Structure

```
├── Heart.ipynb               # EDA, preprocessing, model training & evaluation
├── heart.csv                 # Dataset
└── README.md
```
⭐ If you found this project useful, consider giving it a star!
