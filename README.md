# Predicting Vehicle CO2 Emissions using Linear Regression

## Project Overview

This project uses a Linear Regression model to predict the carbon dioxide (CO2) emissions of various vehicles based on their specifications. The goal is to build a simple yet effective model that can estimate CO2 output from features like engine size, number of cylinders, and fuel consumption.

This project serves as a practical example of a complete regression workflow, including data cleaning, outlier handling, feature scaling, model training, and performance evaluation with standard regression metrics.

## Dataset

The project utilizes the **"Fuel Consumption Ratings"** dataset.

* **Source File:** `FuelConsumption.csv`
* **Description:** The dataset contains model-specific fuel consumption ratings and estimated carbon dioxide emissions for new light-duty vehicles for retail sale in Canada.

## Project Workflow

1.  **Data Loading and Cleaning:**
    * The `FuelConsumption.csv` dataset is loaded into a pandas DataFrame.
    * Column names are programmatically cleaned by removing spaces and standardizing them for easy access.

2.  **Exploratory Data Analysis (EDA):**
    * Initial analysis is conducted to understand the data's structure, statistics, and to check for missing values.

3.  **Feature Selection:**
    * A subset of relevant numerical features (`ENGINESIZE`, `CYLINDERS`, `FUELCONSUMPTION_COMB`, etc.) is selected for the model. Categorical and non-essential columns are dropped.

4.  **Outlier Detection and Removal:**
    * Numerical features are visualized using box plots to identify outliers.
    * The Interquartile Range (IQR) method is employed to filter out these outliers, leading to a more robust model. The data is visualized again post-removal to confirm the effect.

5.  **Data Visualization:**
    * Histograms are plotted for all features to visualize their distributions after the cleaning process.

6.  **Data Splitting and Scaling:**
    * The cleaned dataset is split into an 80% training set and a 20% testing set.
    * All features are scaled using `StandardScaler` to ensure they are on a comparable scale.

7.  **Model Training:**
    * A `LinearRegression` model from Scikit-learn is trained on the preprocessed training data.

8.  **Model Evaluation:**
    * The trained model's performance is evaluated on the test set using standard regression metrics:
        * **R-squared:** To measure the proportion of variance in the target variable that can be predicted from the features.
        * **Mean Absolute Error (MAE):** The average absolute difference between predicted and actual values.
        * **Mean Squared Error (MSE):** The average of the squares of the errors.
        * **Root Mean Squared Error (RMSE):** The square root of the MSE, providing an error metric in the same units as the target variable.

9.  **Results Visualization:**
    * A scatter plot is created to visually compare the `Actual` CO2 emissions against the model's `Predicted` values, providing a clear indication of the model's accuracy.

## Technologies Used

* Python 3
* Pandas & NumPy
* Scikit-learn
* Matplotlib & Seaborn
* Jupyter Notebook / Google Colab

## How to Run This Project

1.  **Download Files:** Obtain the project notebook (`.ipynb` file) and the `FuelConsumption.csv` dataset.
2.  **Setup Environment:** Open the notebook in a compatible environment like Google Colab or Jupyter. Upload the `FuelConsumption.csv` file.
3.  **Execute Code:** Run the cells of the notebook sequentially to perform the data analysis, train the model, and evaluate its performance.

## Conclusion

The project successfully demonstrates the application of Linear Regression for a real-world prediction task. The final model is capable of predicting vehicle CO2 emissions with a high degree of accuracy, as evidenced by the strong R-squared value and the tight clustering of points around the diagonal in the final prediction plot.
