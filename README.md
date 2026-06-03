# Elevate Labs AI & ML Internship - Task 3

## Project Objective
Implementation and evaluation of a Linear Regression model to predict house prices using Python and Scikit-Learn.

## Workflow & Methodology
1. **Library & Tool Setup:** Imported key data science packages including `pandas`, `numpy`, `matplotlib`, and `sklearn`.
2. **Dataset Generation:** Created a synthetic housing dataset representing relationships between house sizes (Square Feet) and their market prices.
3. **Train-Test Split:** Partitioned the dataset using an 80/20 split (`train_test_split`) to ensure separate data for training and evaluation.
4. **Model Training:** Initialized and fitted a `LinearRegression` model using Scikit-Learn to compute the optimal line of best fit.
5. **Performance Evaluation:** Evaluated prediction errors using standard metrics: Mean Absolute Error (MAE), Mean Squared Error (MSE), and the R-squared ($R^2$) score.
6. **Visualization:** Plotted the calculated regression line alongside the true test data points using Matplotlib.

## Interview Questions & Core Concepts

### 1. What assumptions does linear regression make?
* **Linearity:** Assumes a straight-line relationship exists between the independent (input) and dependent (output) variables.
* **Independence:** Assumes that data observations are independent of each other.
* **Homoscedasticity:** Assumes that the residuals (errors) have a constant variance across all levels of the independent variables.
* **Normality:** Assumes that the residual errors are normally distributed.

### 2. How do you interpret the coefficients?
The coefficient represents the slope of the regression line. It tells us how much the target variable ($y$) is expected to change for every single unit increase in the predictor feature ($X$), assuming all other variables remain constant.

### 3. What is $R^2$ score and its significance?
The $R^2$ score (Coefficient of Determination) measures the proportion of variance in the target variable that is predictable from the input features. It ranges from 0 to 1; a higher score indicates a stronger fit, meaning the model explains a large percentage of the data's variation.

### 4. When would you prefer MSE over MAE?
Mean Squared Error (MSE) squares the errors before averaging them, which heavily penalizes larger errors or outliers. You prefer MSE when large prediction errors are particularly undesirable or dangerous to your project goal. Mean Absolute Error (MAE) is preferred when you want a steady, linear reflection of average error without over-emphasizing extreme anomalies.

### 5. How do you detect multicollinearity?
Multicollinearity occurs when two or more independent features are highly correlated with each other. It can be detected using:
* **Correlation Matrix:** Looking for high correlation coefficients (e.g., above 0.8) between independent variables.
* **Variance Inflation Factor (VIF):** A mathematical score where a VIF value greater than 5 or 10 suggests significant multicollinearity.

### 6. What is the difference between simple and multiple regression?
* **Simple Linear Regression:** Uses exactly **one** independent feature to predict a target variable (e.g., predicting house price using *only* Square Feet).
* **Multiple Linear Regression:** Uses **two or more** independent features to predict a target variable (e.g., predicting house price using Square Feet, *plus* Number of Bedrooms, *plus* Neighborhood Safety Rating).

### 7. Can linear regression be used for classification?
No, linear regression is designed for predicting continuous, numeric values (like prices or temperatures). For classification tasks (predicting categories like "Yes/No" or "Spam/Not Spam"), **Logistic Regression** or other classification algorithms are used instead.

### 8. What happens if you violate regression assumptions?
Violating these assumptions means the model's statistical tests, confidence intervals, and coefficient calculations can become unstable, inaccurate, or deeply biased. It reduces the trustworthiness and predictive reliability of the model on new, unseen data.
