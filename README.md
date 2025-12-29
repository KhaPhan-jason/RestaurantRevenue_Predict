# Restaurant Revenue Prediction

This project performs **exploratory data analysis (EDA)** and **predictive modeling** to estimate restaurant revenue. The analysis identifies key factors affecting revenue and builds a linear regression model to predict restaurant earnings.

---

## Dataset

- **File:** `restaurant_data.csv`
- **Key Columns:**  
  `Location`, `Cuisine`, `Average Meal Price`, `Seating Capacity`,  
  `Weekend Reservations`, `Weekday Reservations`, `Revenue`
- **Preprocessing:**  
  - Checked for duplicates and missing values  
  - Encoded categorical variables using LabelEncoder:  
    - `Location`: Downtown=0, Rural=1, Suburban=2  
    - `Cuisine`: American=0, French=1, Indian=2, Italian=3, Japanese=4, Mexican=5  

---

## Libraries

- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `scipy`

---

## Exploratory Data Analysis (EDA)

1. **Overview**  
   - Checked dataset shape, data types, missing values, and duplicates  

2. **Categorical Features**  
   - `Location` and `Cuisine` analyzed using pie charts and ANOVA  
   - Both variables significantly influence revenue  

3. **Numeric Features**  
   - `Average Meal Price`, `Seating Capacity`, `Weekend Reservations`, `Weekday Reservations`, `Revenue` analyzed using histograms and boxplots  
   - Correlation analysis identified numeric features most related to revenue  

4. **Correlation Insights**  
   - Strongest correlations with `Revenue`:  
     - `Average Meal Price`  
     - `Seating Capacity`  

5. **Visualization Insights**  
   - Restaurants in Downtown areas and certain cuisines generate higher revenue  
   - Revenue increases with higher seating capacity and average meal price  
   - Weekend and weekday reservations also positively influence revenue  

---

## Predictive Modeling

- **Model:** Linear Regression  
- **Features:** `Location`, `Cuisine`, `Average Meal Price`, `Seating Capacity`, `Weekend Reservations`, `Weekday Reservations`  
- **Target:** `Revenue`  
- **Train/Test Split:** 80% training, 20% testing  

### Model Performance

- **Full R² (all data):** [model.score(X, y)]  
- **Train R²:** [model.score(X_train, y_train)]  
- **Test R²:** [model.score(X_test, y_test)]  
- Coefficients indicate the impact of each feature on revenue  

---

## Insights

- **Key Revenue Drivers:**  
  - Restaurants in Downtown areas tend to have higher revenue  
  - Cuisine type significantly affects earnings, with some cuisines generating more revenue than others  
  - Higher average meal price and larger seating capacity increase revenue  
  - More reservations on weekdays and weekends positively affect revenue  

- **Model Insights:**  
  - Linear regression captures the main factors affecting revenue  
  - Categorical and numeric features together explain a large portion of revenue variance  

- **Overall:**  
  Revenue prediction can be effectively estimated using restaurant location, cuisine, pricing, seating capacity, and reservation patterns. The model can help owners make data-driven decisions to optimize revenue.
