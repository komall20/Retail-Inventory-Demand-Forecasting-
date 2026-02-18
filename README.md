# 🛒 Retail Demand Forecasting with XGBoost

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Library](https://img.shields.io/badge/Library-XGBoost-orange)
![Status](https://img.shields.io/badge/Status-Completed-green)

## 📌 Business Problem
In the retail sector, inventory mismanagement is a billion-dollar problem. Overstocking leads to perishability costs, while understocking leads to lost revenue and customer dissatisfaction. 

**The Goal:** Build a predictive model to forecast sales for individual items across 10 different store types, enabling store managers to optimize inventory levels.

## 🚀 Solution Overview
This project implements an end-to-end Machine Learning pipeline using **XGBoost** to predict `Item_Outlet_Sales`. 

**Key Technical Highlights:**
* **Advanced Imputation:** Handled missing `Item_Weight` values using a pivot table logic based on `Item_Identifier` (not just mean/median filling).
* **Feature Engineering:** * Created `Outlet_Years` to capture the maturity of a store.
    * Modified `Item_Visibility` to handle zero-values by imputing them with the mean visibility of that product.
* **Model Selection:** Benchmarked Linear Regression, Random Forest, and XGBoost. XGBoost was selected for its superior handling of non-linear relationships.

## 📊 Key Insights & Results
The model achieved an **RMSE of 1240.2463** on the test set.

**1. Visibility Paradox:**
Contrary to popular belief, items with *higher* visibility often showed slightly *lower* sales. This suggests customers prioritize "Need-based" shopping (grabbing essentials) over "Impulse" shopping for this specific product mix.

**2. Store Maturity Matters:**
Stores established longer ago (`Outlet_Years` > 20) showed significantly higher sales volume, indicating a strong customer loyalty factor.

![Feature Importance](images/feature_importance.png)

## 🛠️ Tech Stack
* **Language:** Python
* **ML Engine:** XGBoost, Scikit-Learn
* **Data Processing:** Pandas, NumPy
* **Visualization:** Seaborn, Matplotlib

## 💻 How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/komall20/Retail-Inventory-Demand-Forecasting.git](https://github.com/komall20/Retail-Inventory-Demand-Forecasting.git)
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
3. Run the notebook:
   ```bash
   jupyter notebook Mart_Sales.ipynb

📜 License
This project is licensed under the MIT License.
