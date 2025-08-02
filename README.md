# 🩺 Lung Cancer Prediction using Logistic Regression

This project uses **Logistic Regression** to predict whether a person is likely to have lung cancer, based on survey data of symptoms and habits such as smoking, anxiety, fatigue, etc.

It includes **data preprocessing**, **model training**, **evaluation**, and **visualizations** using Python libraries like pandas, seaborn, and scikit-learn.

---

## 📦 Dataset

- **Source:** [Lung Cancer Survey Dataset](https://raw.githubusercontent.com/mgsalama/Lung-Cancer-Classification/main/survey_lung_cancer.csv)
- **Size:** 309 rows × 16 columns
- **Target Column:** `LUNG_CANCER` (values: `YES` or `NO`)
- **Features Include:**
  - Age, Gender
  - Smoking, Alcohol consumption
  - Yellow fingers, Wheezing, Coughing
  - Shortness of breath, Chest pain, and more

---

## 🧪 Workflow Overview

### ✅ 1. **Data Loading and Cleaning**
- Loaded the dataset from a public GitHub URL.
- Converted categorical values:
  - `YES` → `1`, `NO` → `0`
  - `M` (male) → `1`, `F` (female) → `0`
  - Binary feature values were standardized (2 → 0).

### 🧼 2. **Preprocessing**
- Removed extra spaces from column names.
- Separated the features (`X`) and target (`y`).
- Performed **train-test split** with stratification (70:30).

### 🧠 3. **Model Building**
- Trained a **Logistic Regression** model using scikit-learn with increased iterations.
- Checked:
  - Model coefficients
  - Intercept (bias)

### 📊 4. **Evaluation**
- Accuracy: **90.3%**
- Confusion Matrix
- Classification Report (Precision, Recall, F1-score)

### 📈 5. **Visualizations**
- Heatmap of Feature Correlation
- Confusion Matrix
- Class Distribution of Target Variable

---

## 📊 Model Performance

| Metric        | Value          |
|---------------|----------------|
| Accuracy      | 90.32%         |
| Precision (1) | 93%            |
| Recall (1)    | 96%            |
| F1-score (1)  | 95%            |

- Class `1`: Lung cancer **present**
- Class `0`: Lung cancer **not present**

---

## 📌 Sample Visuals

### 🔵 Confusion Matrix

Actual 0 vs Predicted 0: 6
Actual 0 vs Predicted 1: 6
Actual 1 vs Predicted 0: 3
Actual 1 vs Predicted 1: 78


### 📉 Correlation Heatmap  
- Shows how each symptom is related to others and to the target.

### 📊 Target Distribution  
- 270 out of 309 entries are labeled `YES` (imbalanced dataset)

---

## 🧰 Tools & Libraries Used

- `pandas`, `numpy` for data handling
- `matplotlib`, `seaborn` for visualization
- `scikit-learn` for model building and evaluation
- `Google Colab` as the runtime environment

---

## ▶️ How to Run the Project

1. Open the code in **Google Colab** or Jupyter Notebook.
2. Install required libraries if needed:
   ```bash
   pip install pandas seaborn scikit-learn matplotlib
3. Run the notebook step-by-step.
4. Observe prediction performance and visual insights.

🧠 What You Learn
How to clean and preprocess health data

Apply logistic regression for binary classification

Evaluate using accuracy, confusion matrix, and classification report

Visualize correlations and class distributions

