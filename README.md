# 🏡 Real Estate Price Prediction using Neural Network

## 📋 Project Overview
This project aims to build a **regression model to predict listing prices** using multiple numerical features such as ratings, reviews, bathrooms, bedrooms, guests, etc. The project leverages a **Dense Neural Network (DNN)** to model the complex relationships between the provided features and the target price.

---
## 📦 Dataset

The dataset used for this project contains listing information such as ratings, reviews, bedrooms, bathrooms, guests, etc.

- **Dataset link**: [Download Dataset](https://drive.google.com/drive/folders/1b4wyeI3MGDZXzKx0KR0ZTy6-lPAPBIuK)


## 📊 Dataset Description
The dataset contains the following features:
- `rating`: Listing rating.
- `reviews`: Number of reviews.
- `bathrooms`: Number of bathrooms.
- `beds`: Number of beds.
- `guests`: Guest capacity.
- `toiles`: Number of toilets.
- `bedrooms`: Number of bedrooms.
- `studios`: Number of studios.
- `country`: Encoded country (numerical).

### Target Variable:
- `price`: Price of the listing (continuous numerical value).

---

## 🔧 Approach

### 1. Data Preprocessing
- Duplicate entries were **retained intentionally** to preserve dataset size and pattern diversity.
- The target variable `price` was **normalized** to stabilize the model training process.
- All features were treated as numerical and used directly in the model.

### 2. Model Building
- A **Sequential Dense Neural Network** was implemented using Keras.
  - Multiple hidden layers with **ReLU activation**.
  - Output layer with **linear activation** suitable for regression.

### 3. Model Evaluation
As this is a **regression problem**, the following metrics were used:
- **Mean Absolute Error (MAE)**
- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**
- **R² Score**

⚠ Note:  
Classification metrics like accuracy, precision, recall, and AUC-ROC were **not used**, as they are not applicable to regression tasks.

---

## 📈 Results
- The model achieved an **R² score of approximately (insert your R² here)**.
- The **validation loss was slightly higher**, which is normal due to the **normalization of the target price**.
- The use of duplicate entries ensured that the dataset was not too small and allowed the model to learn from diverse feature patterns.

---

## ✅ Conclusion
- Retaining duplicates helped in keeping the dataset size larger, leading to better feature interaction and model learning.
- Target normalization contributed to stable learning, despite slightly higher validation loss, which is acceptable in such scenarios.
- Future improvements can include:
  - **Feature engineering (interaction terms, categorical handling).**
  - **Outlier detection and removal.**
  - **Exploring other regression models like Random Forest, XGBoost.**

---

## 💡 Technologies Used
- Python
- Pandas
- Numpy
- Scikit-Learn
- Keras (TensorFlow backend)
- Matplotlib, Seaborn

---

