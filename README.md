# 🌬️ Wind Power Generation Forecasting

## 1. Title
**Wind Power Generation Forecasting using Machine Learning**

---

## 2. Executive Summary

- **Business Problem:**  
Wind energy is highly dependent on weather conditions, making it difficult to accurately predict power generation for grid stability and energy planning.

- **Solution:**  
Built a machine learning pipeline using meteorological features (wind speed, humidity, temperature, etc.) to forecast wind power generation.

- **Next Steps:**  
Improve accuracy using advanced models (LSTM, time-series models) and deploy the model for real-time forecasting.

- **Impact (Numbers):**
  - Best Model: **Tuned XGBoost**
  - R² Score: **0.643**
  - MAE: **0.113**
  - MSE: **0.0238**

---

## 3. Business Problem

Accurate prediction of wind power generation is critical for:

- Efficient grid management  
- Reducing energy wastage  
- Planning renewable energy supply  

Traditional forecasting methods fail to capture complex weather interactions, making ML-based prediction essential.

---

## 4. Methodology

### 🔹 Data Collection & Preparation

- Combined 4 datasets (`Location1–4`)
- Total dataset size: **175,200 records**
- Features include:
  - Temperature, Humidity, Dew Point  
  - Wind Speed (10m & 100m)  
  - Wind Direction  
  - Wind Gusts  
  - Power (Target variable)

---

### 🔹 Exploratory Data Analysis

- Performed distribution analysis using histograms  
- Identified outliers using boxplots  
- Analyzed relationships using scatter plots  
- Used correlation matrix to identify key predictors  

---

### 🔹 Key Insights from EDA

- Strong correlation:
  - `windspeed_100m` → Power (**0.62**)  
  - `windgusts_10m` → Power (**0.57**)  

- Weak correlation:
  - Temperature & humidity have minimal impact  

- Outliers present in wind-related features  

- Power distribution is right-skewed  

---

## 5. Skills Used

- Python (Pandas, NumPy)  
- Data Visualization (Matplotlib, Seaborn)  
- Machine Learning (Scikit-learn, XGBoost)  
- Feature Engineering  
- Model Evaluation & Hyperparameter Tuning  

---

## 6. Models & Results

### 🔹 Linear Regression

- MAE: **0.1377**  
- MSE: **0.0325**  
- R² Score: **0.513**

👉 Basic model with moderate performance.

---

### 🔹 Random Forest Regressor

- MAE: **0.1065**  
- MSE: **0.0216**  
- R² Score: **0.677**

👉 Significant improvement due to non-linear learning.

---

### 🔹 XGBoost Regressor

- MAE: **0.1157**  
- MSE: **0.0249**  
- R² Score: **0.626**

👉 Strong performance with gradient boosting.

---

### 🔹 Tuned XGBoost (Best Model 🚀)

**Best Parameters:**
- `learning_rate`: 0.1  
- `max_depth`: 7  
- `n_estimators`: 300  
- `subsample`: 0.8  

**Performance:**
- MAE: **0.1131**  
- MSE: **0.0238**  
- R² Score: **0.643**

👉 Best balance between bias and variance.

---

## 7. Results & Business Recommendations

### 📊 Key Results

- Tree-based models outperform linear models  
- Wind-related features are the strongest predictors  
- Tuned XGBoost provides the most reliable predictions  

---

### 💡 Business Recommendations

- Use the model for **short-term energy forecasting**  
- Focus on **wind speed sensor accuracy**  
- Deploy model for **real-time grid optimization**  
- Use predictions to reduce **energy imbalance penalties**  

---

## 8. Next Steps

- Implement **LSTM / Time Series models**  
- Deploy using **Flask / FastAPI**  
- Integrate **real-time weather APIs**  
- Perform **feature importance analysis**  
- Build **interactive dashboard (Streamlit / Power BI)**  

---

## 9. How to Run the Project

```bash
git clone https://github.com/Abhaypratapsingh22/Wind_Power_Generation_Forecasting.git
cd Wind_Power_Generation_Forecasting
pip install -r requirements.txt
jupyter notebook Wind_Power_Generation.ipynb
