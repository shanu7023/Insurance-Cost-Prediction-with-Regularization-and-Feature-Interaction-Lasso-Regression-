# 💰 Medical Cost Prediction using Lasso Regression

## 📌 Project Overview

This project aims to predict individual medical insurance costs using machine learning techniques. Accurate prediction helps insurance companies set premiums and assists individuals in financial planning.

---

## 📊 Dataset

The dataset includes:

* Age, Sex, BMI (physical attributes)
* Children (number of dependents)
* Smoker (high impact feature)
* Region (categorical location feature)

Target Variable:

* Charges (medical cost)

---

## 🛠️ Feature Engineering

* One-Hot Encoding:

  * Converted categorical variables (region) into numerical format

* Interaction Features:

  * `age_smoker`
  * `bmi_smoker`

These features capture the combined effect of smoking with age and BMI, improving model performance.

---

## 🤖 Model Used: Lasso Regression

### Why Lasso?

* Performs regularization to reduce overfitting
* Automatically selects important features by shrinking less important coefficients to zero

---

## 🔍 Hyperparameter Tuning

* Used **LassoCV** with 5-fold cross-validation
* Tested alpha values from 0.001 to 100
* Automatically selected optimal alpha

---

## 📈 Model Performance

* Best Alpha: 0.001
* R² Score: 0.865
* Mean Squared Error (MSE): 20,922,599

---

## 📉 Visualization

### Alpha vs MSE Curve

This graph shows how model error changes with different alpha values.

![Lasso Regression Alpha vs MSE](alpha_vs_mse_plot.png) <img width="556" height="428" alt="image" src="https://github.com/user-attachments/assets/34b33ccd-4878-49d6-bcbd-a4bd67543427" />


* Low alpha → complex model (risk of overfitting)
* High alpha → simpler model (risk of underfitting)
* Optimal alpha balances both

As Alpha increases, we observe the penalty simplifying the model. The optimal Alpha was found to be 0.001 , where the test MSE was at its lowest.

---

## 📌 Key Insights

* Smoking status has a significant impact on insurance cost
* Interaction features improved model performance
* Lasso successfully reduced irrelevant feature influence

---

## 🛠️ Tech Stack

* Python
* Pandas
* NumPy
* Scikit-learn
* Seaborn

---

## 🚀 Future Improvements

* Compare with Linear Regression and Ridge Regression
* Use advanced models (XGBoost)
* Feature scaling optimization
* Deploy model using Streamlit

---

## 📁 Project Structure

* insurance.csv
* Lasso Regression.ipynb
* README.md
* alpha_vs_mse_plot.png

---

## 👨‍💻 Author

Shanu






















