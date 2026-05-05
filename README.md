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

## 📉 Visualizations

### Hyperparameter Tuning: Alpha vs. MSE
The plot below illustrates how the model's Mean Squared Error (MSE) changes as the regularization strength (**Alpha**) increases.




![Lasso Regression Alpha vs MSE](alpha_vs_mse_plot.png) <img width="556" height="428" alt="image" src="https://github.com/user-attachments/assets/34b33ccd-4878-49d6-bcbd-a4bd67543427" />

"As Alpha increases, we observe the penalty simplifying the model. The optimal Alpha was found to be 0.001 , where the test MSE was at its lowest."

**Key Takeaway:** 
By visualizing the error curve, we can identify the "elbow" point where the model achieves the best balance between bias and variance. The **LassoCV** implementation automatically selected the Alpha value that minimized this error, ensuring the most robust predictions on unseen data.
