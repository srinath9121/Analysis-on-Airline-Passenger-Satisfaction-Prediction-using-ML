# Airline Passenger Satisfaction - Classification



# ✈️ Airline Passenger Satisfaction Prediction

## 1. Overview
This project predicts airline passenger satisfaction using survey data from thousands of flights.  
It demonstrates an **end-to-end ML workflow**: from **EDA → preprocessing → model training → hyperparameter tuning → evaluation**.  
The repository is structured for clarity, reproducibility, and professional presentation.

---

## 2. Dataset
Source: [Kaggle - Airline Passenger Satisfaction](https://www.kaggle.com/datasets/mysarahmadbhat/airline-passenger-satisfaction)  

**Features:**
- **Demographics:** Gender, Age, Customer Type  
- **Travel Info:** Type of Travel, Class, Flight Distance  
- **Service Ratings (1–5):** Inflight wifi, Food & drink, Online boarding, Seat comfort, etc.  
- **Delays:** Departure Delay, Arrival Delay  
- **Target:** Satisfaction (Satisfied / Neutral or Dissatisfied)

Dataset description is in [`data/README.md`](./data/README.md).

---

## 3. Methodology
1. **Exploratory Data Analysis (EDA):**  
   - Heatmaps, boxplots, satisfaction distribution.  
   - Correlation of service ratings with satisfaction.  

2. **Preprocessing:**  
   - Handle missing values, encode categoricals, scale numerics.  
   - Apply SMOTE to handle class imbalance.  

3. **Modeling:**  
   - Logistic Regression, Random Forest, Gradient Boosting, XGBoost, SVM, KNN.  
   - Hyperparameter tuning with Stratified KFold + RandomizedSearchCV.  

4. **Evaluation:**  
   - Metrics: Accuracy, Precision, Recall, F1, ROC-AUC, PR-AUC.  
   - Confusion matrices, ROC/PR curves, feature importance plots.  

---

## 4. Results
- **Best Model:** XGBoost (F1 ≈ 0.87, ROC-AUC ≈ 0.91).  
- **Top Predictors:** Travel class, seat comfort, inflight service, departure delays.  
- **Insight:** Service quality has greater influence on satisfaction than delays alone.  

📊 See full details in [`reports/results.md`](./reports/results.md).

---

## 5. Usage

### Installation
```bash
git clone https://github.com/<your-username>/airplane-satisfaction.git
cd airplane-satisfaction
pip install -r requirements.txt
