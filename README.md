# Import necessary libraries
import numpy as np
from sklearn.linear_model import LinearRegression
import pandas as pd

# Load your dataset using pandas
data = pd.read_csv('your_data.csv')  # Replace 'your_data.csv' with your dataset's filename

# Define the independent variable (X) and dependent variable (y)
X = data[['independent_variable_column']]  # Replace 'independent_variable_column' with your actual column name
y = data['dependent_variable_column']      # Replace 'dependent_variable_column' with your actual column name

# Create a linear regression model
model = LinearRegression()

# Fit the model to your data
model.fit(X, y)

# Print the coefficients
print('Intercept:', model.intercept_)
print('Slope:', model.coef_[0])
