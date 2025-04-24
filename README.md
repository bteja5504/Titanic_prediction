# Titanic Survival Prediction Using Machine Learning
## Key Features
1 . Handles missing data (e.g., Age and Embarked)
2 . Encodes categorical features (Sex, Embarked)
3 . Normalizes numerical features (Age, Fare)
4 . Uses a Random Forest Classifier for prediction
5 . Evaluates model performance with:
6 . Accuracy,Precision,Recall,F1 Score,Confusion Matrix
7 . Visualizes feature importance and key relationships
8 . Modular and easy to extend with other models or deployment tools¶

## Importing Libraries

In this project, I **import essential libraries** that play pivotal roles in enhancing data manipulation and visualization capabilities:

- **pandas**: A versatile library for data manipulation and analysis, enabling me to handle tabular data structures effectively.
- **numpy**: A fundamental library for numerical operations and computations, empowering me with efficient mathematical operations on arrays.
- **seaborn**: A powerful data visualization library based on matplotlib, simplifying the creation of informative statistical graphics.
- **matplotlib.pyplot**: A widely used library for creating plots and charts, crucial for visualizing my data and analysis results effectively.

## Loading Data

My project begins with **loading data** from CSV files using the **pandas** library, segregating the data into train and test datasets. These datasets contain crucial information about the Titanic passengers, forming the foundation of my analysis.

## EDA (Exploratory Data Analysis)

Engaging in **Exploratory Data Analysis (EDA)**, I embark on a journey of understanding my dataset deeply. Through various visualization techniques, I:

- **Visualize distributions** of key numerical features like age, number of siblings/spouses (SibSp), number of parents/children (Parch), and fare. This helps me uncover trends and identify outliers.
- **Explore relationships** between different variables, potentially revealing correlations that could impact survival predictions.

## Data Cleaning:

Data cleaning is a pivotal stage in my analysis. In this phase, I:
The Titanic dataset contained several missing and irrelevant fields that needed to be addressed before model training. The following cleaning steps were performed:
1.Age: Missing values were filled using the median age grouped by Pclass and Sex to better reflect realistic age distributions.
2.Fare: Missing values were replaced with the overall median fare.
3.Embarked: Rows with missing embarkation ports were filled with the mode ('S'), the most common port.
4.Cabin: Due to high missingness (~77%), the original Cabin column was dropped. However, a new binary feature HasCabin was created to indicate whether a cabin number was present.
5.Dropped Unnecessary Columns: Columns like Name, Ticket, and PassengerId were removed as they provided little predictive value or were identifiers not needed for model training.
- This can lead to improved predictive performance.
- 
## Model Testing:

My project involves rigorous **model testing** to determine the best approach for predicting passenger survival on the Titanic. I evaluate multiple machine learning models, including Decision Tree, LGBM, XGBoost, RandomForest, ExtraTrees, and Logistic Regression. The culmination of my efforts is a model with an impressive **69.8% accuracy**, showcasing its ability to make accurate predictions.

## Test Submission:

With my chosen model in place, I apply it to predict survival on the test dataset. I then create a **submission file**, a critical step for evaluation purposes, allowing me to see how well my model generalizes to new and unseen data.

## Expected Output:

At a predictive accuracy of **69.8%**, my model demonstrates its potential to forecast Titanic passenger survival effectively. This project not only illustrates the practical application of machine learning techniques on historical data but also provides insights into the influential factors behind survival rates during the Titanic disaster.
