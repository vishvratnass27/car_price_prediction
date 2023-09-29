# car_price_prediction

Certainly! this project  for building and evaluating two different machine learning models: 
a Linear Regression model and a Random Forest Regressor, to predict car prices based on various features. Below is a breakdown of the code along with a simple explanation:

**Code Explanation**:

1. Import necessary libraries:

   - `pandas` for data manipulation.
   - `matplotlib` and `seaborn` for data visualization.
   - `numpy` for numerical operations.
   - `sklearn` for machine learning.
   
2. Load the car dataset from a CSV file using `pd.read_csv()`.

3. Explore the dataset:

   - `car_dataset.head(10)` displays the first 10 rows of the dataset.
   - `car_dataset.info()` provides information about the dataset's structure.
   - `car_dataset.shape` shows the number of rows and columns in the dataset.
   - `y` is set as the target variable, which is the "price" column.

4. Create a feature matrix `X` by selecting specific columns from the dataset, including "year," "distance_travelled(kms)," "brand_rank," and "car_age."

5. One-Hot Encode Categorical Variables:

   - Create dummy variables for categorical variables like "brand," "fuel_type," and "city" using `pd.get_dummies()`.
   - Drop the first category in each dummy variable using `drop_first=True` to avoid multicollinearity.

6. Concatenate the one-hot encoded categorical variables and the selected numerical features to create the final feature matrix `X`.

7. Split the data into training and testing sets using `train_test_split()` from `sklearn`.

8. Train a Linear Regression model and evaluate its performance using Mean Absolute Error (`metrics.mean_absolute_error`) and R-squared (`model.score`).

9. Train a Random Forest Regressor model, evaluate its performance, and calculate feature importances using `feature_importances_`.

10. Create a DataFrame (`car_dataset`) to display the feature importances, sort it in descending order, and visualize the importance of each feature.

**GitHub README**:

Here's a simple GitHub README for this code:

```markdown
# Car Price Prediction

This repository contains code to predict car prices based on various features using machine learning. Two models were used: Linear Regression and Random Forest Regressor.

## How to Use

1. Install the required libraries using `pip install pandas matplotlib seaborn numpy scikit-learn`.

2. Run the code in a Python environment.

3. Adjust the dataset file path if necessary.

4. Explore the model performance, feature importance, and evaluation metrics.

## Code Explanation

- Load and explore the car dataset.
- One-hot encode categorical variables.
- Split the data into training and testing sets.
- Train and evaluate a Linear Regression model.
- Train and evaluate a Random Forest Regressor model.
- Display feature importances and their rankings.

## Contributors

- vishvratna shegaonkar



