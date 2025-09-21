# 🌸 Diabetes Progression – Linear Regression Analysis

## 📌 Project Overview
This project applies **Linear Regression** to predict **diabetes disease progression** based on patient attributes.  
We evaluate the model using **R² score** and visualize predictions versus actual outcomes to assess performance.  

---

## 📂 Dataset
- **Source:** `diabetes_dirty.csv`  
- **Features:**  
  - AGE: Patient age in years  
  - SEX: 1 = female, 2 = male  
  - BMI: Body mass index  
  - BP: Blood pressure  
  - S1–S6: Six blood serum measurements  
- **Target:** PROGRESSION – quantitative measure of disease progression  

**Sample data:**
| AGE | SEX | BMI  | BP  | S1  | S2    | S3   | S4  | S5    | S6 | PROGRESSION |
|-----|-----|------|-----|-----|-------|------|-----|-------|----|-------------|
| 59  | 2   | 32.1 | 101 | 157 | 93.2  | 38.0 | 4.0 | 4.8598 | 87 | 151         |
| 48  | 1   | 21.6 | 87  | 183 | 103.2 | 70.0 | 3.0 | 3.8918 | 69 | 75          |
| 72  | 2   | 30.5 | 93  | 156 | 93.6  | 41.0 | 4.0 | 4.6728 | 85 | 141         |

---

## ⚙️ Approach
1. **Data Preprocessing**  
   - Split data into training (80%) and test (20%) sets.  
   - Applied **MinMaxScaler** and **StandardScaler** to compare scaling effects.  

2. **Model Training**  
   - Linear Regression (`sklearn.linear_model.LinearRegression`) trained on standardized features.  

3. **Evaluation**  
   - Model coefficients and intercept inspected.  
   - R² score computed on test set.  
   - Actual vs. predicted progression plotted to visualize alignment.  

---

## 📊 Results
**Model Parameters:**
- **Intercept:** 153.7365  
- **Coefficients:** `[1.754, -11.512, 25.607, 16.829, -44.449, 24.641, 7.677, 13.139, 35.161, 2.351]`  

**R² Score on Test Set:** 0.4526  

**Scatter Plot – Actual vs Predicted:**

![Actual vs Predicted](scatter_plot.png)  

**Interpretation:**  
- The R² score (~0.45) indicates the model explains ~45% of the variance in disease progression.  
- The scatter plot shows a **moderate alignment** with the diagonal line, meaning the model captures general trends but lacks precise predictions for all cases.  
- Spread around the line suggests other factors or more complex models may improve prediction accuracy.  

---

## ✅ Key Takeaways
- Linear Regression provides a **baseline prediction** for diabetes progression.  
- Standardization helps the model handle features with different scales.  
- Including additional features or using **advanced models** (e.g., Random Forest, Gradient Boosting, Neural Networks) could improve performance.  

---

## 🛠️ Tech Stack
- **Language:** Python  
- **Libraries:** pandas, numpy, scikit-learn, matplotlib  

---

## 👨‍💻 Author
**AiVintage (Veli)**  
Data Science Graduate | Skilled in Python, Machine Learning, AI, SQL & Data Analysis  
[GitHub](https://github.com/AiVintage) | [LinkedIn](#)
