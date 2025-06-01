# Predict_Calorie-Expenditure

# 🥗 Calorie Prediction Model

This project aims to accurately predict the number of calories burned based on individual biometric and activity features using advanced ensemble machine learning techniques.

## 📌 Project Overview

In this project, we perform regression modeling to estimate the number of calories burned, using features like age, sex, height, weight, heart rate, body temperature, and exercise duration. We apply three powerful models — **Random Forest**, **LightGBM**, and **CatBoost** — and combine their predictions using a **Stacking Regressor** with **XGBoost** as the meta-model.

---

## 📁 Dataset

The dataset contains biometric and activity information of individuals, split into:

- `train.csv`: Contains both features and target (`Calories`)
- `test.csv`: Contains only features, used for generating predictions

### 🎯 Features

| Column      | Description               |
|-------------|---------------------------|
| `id`        | Unique identifier         |
| `Sex`       | Gender of the individual  |
| `Age`       | Age in years              |
| `Height`    | Height in centimeters     |
| `Weight`    | Weight in kilograms       |
| `Duration`  | Exercise duration (mins)  |
| `Heart_Rate`| Avg heart rate during exercise |
| `Body_Temp` | Body temperature (°F)     |
| `Calories`  | 🔺 Target variable         |

---

## ⚙️ Workflow

### ✅ 1. Exploratory Data Analysis (EDA)
- Univariate and bivariate analysis
- Outlier Detection
- Distribution checks for numeric features
- Correlation analysis

### 🧹 2. Data Cleaning & Preprocessing
- Encoding categorical features (`Sex`)
- Scaling numerical features using `RobustScaler`
- Train-Test splitting

### 🔧 3. Feature Engineering
- Interaction terms based on domain logic
- Handled skewness if required

### 🧠 4. Model Building

#### Base Models
- **RandomForestRegressor**
- **LGBMRegressor**
- **CatBoostRegressor**

#### Meta Model
- **XGBRegressor** — combines predictions from base models in a stacked ensemble

#### Final Model
- `StackingRegressor` with passthrough enabled

---

## 📈 Final Evaluation

| Metric   | Score   |
|----------|---------|
| RMSE     | 3.5823  |
| MAE      | 2.1463  |
| R² Score | 0.9967  |

📂 **A submission file was generated using predictions on the test dataset.**

---

## 🛠️ Installation & Setup

# 1. Clone the repository
```bash
git clone https://github.com/your-username/calorie-prediction-model.git
cd calorie-prediction-model
```

# 2. Create and activate a virtual environment (optional but recommended)
```bash
python -m venv venv
source venv/bin/activate  # on Windows use `venv\Scripts\activate`
```

# 3. Install dependencies
```bash
pip install -r requirements.txt
```