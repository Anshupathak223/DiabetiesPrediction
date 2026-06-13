# DiabetiesPrediction
# 🩺 Diabetes Prediction using Support Vector Machine (SVM)

A machine learning project that predicts whether a person is diabetic or non-diabetic based on diagnostic health measurements, using a Support Vector Machine (SVM) classifier trained on the PIMA Indians Diabetes Dataset.

---

## 📌 Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Project Workflow](#project-workflow)
- [Technologies Used](#technologies-used)
- [Model Details](#model-details)
- [Results](#results)
- [How to Use](#how-to-use)
- [Project Structure](#project-structure)

---

## Overview

This project builds a binary classification model to predict diabetes using patient health data. It follows a standard machine learning pipeline: data loading, exploratory analysis, preprocessing, model training, evaluation, and prediction on new input.

---

## Dataset

**PIMA Indians Diabetes Dataset**

- **Source:** Originally from the National Institute of Diabetes and Digestive and Kidney Diseases
- **File:** `diabetes.csv`
- **Target Variable:** `Outcome`
  - `0` → Non-Diabetic
  - `1` → Diabetic

### Features

| Feature | Description |
|---|---|
| Pregnancies | Number of times pregnant |
| Glucose | Plasma glucose concentration |
| BloodPressure | Diastolic blood pressure (mm Hg) |
| SkinThickness | Triceps skin fold thickness (mm) |
| Insulin | 2-Hour serum insulin (mu U/ml) |
| BMI | Body mass index (weight in kg / height in m²) |
| DiabetesPedigreeFunction | Diabetes pedigree function |
| Age | Age in years |
| Outcome | Class label (0 or 1) |

---

## Project Workflow

```
1. Data Collection
       ↓
2. Exploratory Data Analysis (EDA)
       ↓
3. Data Preprocessing & Standardization
       ↓
4. Train-Test Split
       ↓
5. Model Training (SVM with Linear Kernel)
       ↓
6. Model Evaluation (Accuracy Score)
       ↓
7. Prediction on New Input Data
```

---

## Technologies Used

| Library | Purpose |
|---|---|
| `numpy` | Numerical computations |
| `pandas` | Data loading and manipulation |
| `scikit-learn` | ML model, preprocessing, and evaluation |

---

## Model Details

- **Algorithm:** Support Vector Machine (SVM)
- **Kernel:** Linear
- **Preprocessing:** StandardScaler (Z-score normalization)
- **Train-Test Split:** 80% training / 20% testing (stratified, random_state=2)

---

## Results

| Dataset | Accuracy |
|---|---|
| Training Data | ~78–79% |
| Test Data | ~77–78% |

> Accuracy may vary slightly depending on the dataset version used.

---

## How to Use

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/diabetes-prediction.git
cd diabetes-prediction
```

### 2. Install Dependencies

```bash
pip install numpy pandas scikit-learn
```

### 3. Add the Dataset

Place `diabetes.csv` in the project directory (or update the path in the notebook).

### 4. Run the Notebook

Open `Diabeties.ipynb` in Jupyter Notebook or Google Colab and run all cells.

### 5. Make a Prediction

To predict for a new patient, update the `input_data` tuple in the last cell:

```python
input_data = (Pregnancies, Glucose, BloodPressure, SkinThickness,
              Insulin, BMI, DiabetesPedigreeFunction, Age)
```

**Example:**

```python
input_data = (5, 116, 74, 0, 0, 25.6, 0.201, 30)
# Output: 'the person is Non Diabetic'
```

---

## Project Structure

```
diabetes-prediction/
│
├── Diabeties.ipynb       # Main Jupyter Notebook
├── diabetes.csv          # Dataset (add manually)
└── README.md             # Project documentation
```

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
