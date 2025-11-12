# 🧠 ML Linear Regression – BigMart Sales Prediction

Predict retail sales for BigMart products using **Machine Learning (Linear Regression)** trained on historical sales data.  
This project explores data preprocessing, feature engineering, and regression modeling to forecast product sales based on various product and outlet attributes.

---

## 🚀 Live Demo
**Cloud Run App:**  
🔗 [ml-linear-regression-bigmart-salesprediction-65827796111.europe-west1.run.app](https://ml-linear-regression-bigmart-salesprediction-65827796111.europe-west1.run.app/)


## 📊 Project Overview
BigMart Sales Prediction is a supervised regression problem.  
This project focuses on:
- Exploratory Data Analysis (EDA) & visualization.
- Data preprocessing (missing values, outliers, normalization).
- Feature engineering (log transforms, ratio features).
- Model training using **Linear Regression**.
- Model evaluation with RMSE, R².
- Containerized deployment to **Google Cloud Run**.

---

## 🧩 Repository Structure
ML-Linear_Regression-Bigmart-SalesPrediction/
│
├── data/ # Raw and processed datasets
├── notebooks/ # Jupyter notebooks for EDA & modeling
├── src/ # Python scripts for preprocessing & prediction
├── model/ # Serialized trained model (Pickle / Joblib)
├── Dockerfile # For containerizing the app
├── app.py # Flask / FastAPI entrypoint for deployment
├── requirements.txt # Python dependencies
└── README.md # You are here

🧠 Example Prediction
<details> <summary>Click to expand example</summary>
Sample Request
curl -X POST "https://ml-linear-regression-bigmart-salesprediction-65827796111.europe-west1.run.app/predict" \
  -H "Content-Type: application/json" \
  -d '{
        "Item_Weight": 12.8,
        "Item_Visibility": 0.065,
        "Item_MRP": 249.8,
        "Outlet_Establishment_Year": 2002,
        "Outlet_Size": "Medium",
        "Outlet_Location_Type": "Tier 2",
        "Outlet_Type": "Supermarket Type1"
      }'
Sample Response
{
  "predicted_sales": 3720.45
}

📈 Model Training
Algorithm: Linear Regression
Evaluation Metrics: RMSE, R² Score
Preprocessing Steps:
Missing value imputation (mean / KNN)
Log transforms for skewed variables
Feature scaling (standardization)
Categorical encoding (Label/One-Hot)
Ratio features (e.g. visibility ratio)


