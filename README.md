📌 Project Overview
This project aims to predict the individual medical costs billed by health insurance. Predictive modeling in healthcare is crucial for helping companies set premiums and helping individuals plan for future expenses.

In this project, I utilize Lasso Regression to handle feature selection and LassoCV to optimize the model's performance by finding the best regularization strength.

📊 The Dataset
The dataset includes several key features:

Age/Sex/BMI: Physical characteristics.

Children: Number of dependents.

Smoker: Whether the individual smokes (a high-impact feature).

Region: The beneficiary's residential area in the US.

🛠️ Feature Engineering
To improve accuracy, I implemented specific transformations:

One-Hot Encoding: Converted categorical region data into numerical format.

Interaction Terms: Created age_smoker and bmi_smoker. These terms are vital because the cost of smoking isn't just a flat fee; its impact increases significantly as age and BMI increase.

🤖 The Model: Lasso Regression
I chose Lasso (Least Absolute Shrinkage and Selection Operator) because:

Regularization: It prevents the model from overfitting to the training data.

Automatic Feature Selection: Lasso can shrink the coefficients of less important features to zero, effectively simplifying the model.

Hyperparameter Tuning
Using LassoCV with 5-fold Cross-Validation, I tested a range of alpha values from 0.001 to 100 to find the mathematical "sweet spot" for the penalty term.

📈 Performance Results
Best Alpha Found: 0.001

Mean Squared Error (MSE): 20922599.87103596

R² Score: 0.8652317499151699
