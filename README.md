# **Walmart Sales Forecasting**  
*Predicting weekly store sales using Machine Learning (Linear Regression & XGBoost)*  

---

## **Overview**  
Accurate sales forecasting helps retailers optimize inventory, reduce costs, and improve decision-making.  
In this project, we use Walmart’s historical data (2010–2012) to predict weekly store sales, considering:  
- Economic factors (temperature, fuel price, CPI, unemployment).  
- Seasonality and holidays (Super Bowl, Thanksgiving, Christmas).  
- Lag features, rolling averages, and engineered interactions.  

---

## **Dataset**  
**Period:** February 2010 – November 2012  
**Features:**  
  - Store information  
  - Holiday flags  
  - Economic indicators  
  - Engineered features (lags, rolling means, interactions)  
**Target:** Weekly_Sales  

---

## **Methodology**  

1. **Exploratory Data Analysis:** Identifying trends, holiday effects, and store-level patterns.  
2. **Feature Engineering:** Lag variables, rolling means, seasonal and interaction features.  
3. **Modeling:**  
   - Linear Regression as a baseline.  
   - XGBoost as the main model.  
4. **Evaluation:** RMSE, MAE, R², accuracy (±10%), cross-validation, and scenario testing.  

---

## **Results**  
**Linear Regression:** RMSE ≈ `43,410` | MAE ≈ `30,335`  
**XGBoost:** RMSE ≈ `17,634` | MAE ≈ `13,092` | R² ≈ `0.999` | Accuracy (±10%) ≈ `0.9995`  
**Cross-validated RMSE:** ≈ `51,423`  

**Key Insights:**  
Super Bowl increases sales by ~32,000.  
Extreme cold decreases sales by ~44,000.  
Errors are ~50% higher on holiday weeks but stable across stores (max error ~25,000 for sales ~1–2M).  

---

## **Scenario Testing**  
| Scenario       | Predicted Sales |  
|---------------|----------------|  
| Regular Week  | 1,972,427       |  
| Super Bowl    | 2,004,733       |  
| Extreme Cold  | 1,928,078       |  

---

## **How to Run**  
```bash
git clone <repo-link>
pip install -r requirements.txt
python main.py

---

✨ Project by Aliya 🎀
Bringing data to life, one model at a time.


