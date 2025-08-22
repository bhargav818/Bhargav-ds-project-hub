# Revenue Prediction Project

This project is a machine learning pipeline designed to predict revenue for restaurant chains based on various business and operational features. The analysis walks through a classic regression workflow, including data preprocessing, exploratory data analysis, feature engineering, model building, and evaluation.

## Table of Contents

- [Project Description](#project-description)
- [Dataset](#dataset)
- [Project Workflow](#project-workflow)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [License](#license)
- [Acknowledgments](#acknowledgments)

---

## Project Description

**Objective:**  
Predict the revenue of restaurants using business and operational data such as franchise status, menu category, city, number of items, and order volume.

**Tools & Libraries:**
- Python (Jupyter Notebook)
- pandas, numpy
- matplotlib, seaborn
- scikit-learn

---

## Dataset

- **Source:** `revenue_prediction.csv`
- **Features:**
  - `Name`: Restaurant name
  - `Franchise`: Whether the restaurant is a franchise (Yes/No)
  - `Category`: Menu category (e.g., Pizza, BBQ, Sports Bar, etc.)
  - `City`: City where the restaurant operates
  - `No_Of_Item`: Number of items offered
  - `Order_Placed`: Number of orders placed (in thousands)
  - `Revenue`: **Target variable** — Revenue generated

---

## Project Workflow

1. **Data Loading & Initial Exploration**
   - Load the dataset and view initial records.
   - Check for missing data and duplicates.

2. **Data Cleaning & Preprocessing**
   - Remove unnecessary columns (e.g., `Id`).
   - Encode categorical variables using `LabelEncoder`.
   - Final dataset consists of only numerical features.

3. **Feature Selection**
   - Drop columns not contributing to prediction (e.g., `Name`).

4. **Train-Test Split**
   - Split the data into training (80%) and test (20%) sets.

5. **Model Building**
   - Use `LinearRegression` from scikit-learn to fit the model.

6. **Model Evaluation**
   - Evaluate performance using:
     - RMSE (Root Mean Squared Error)
     - MAPE (Mean Absolute Percentage Error)
     - R² Score

7. **Visualization**
   - Use seaborn/matplotlib for exploratory data analysis and results visualization.

---

## Installation

1. Clone the repository or download the notebook and dataset.
2. Install dependencies via pip:

    ```bash
    pip install numpy pandas matplotlib seaborn scikit-learn
    ```

3. Open the Jupyter Notebook:

    ```bash
    jupyter notebook Revenue\ Prediction\ Project.ipynb
    ```

---

## Usage

1. Place the `revenue_prediction.csv` file in the working directory.
2. Run each cell in the Jupyter Notebook (`Revenue Prediction Project.ipynb`) to follow the workflow.
3. Review the outputs, visualizations, and model performance statistics.

---

## Results

- **Model:** Linear Regression
- **Performance on Test Set:**
  - **RMSE:** ~446,367
  - **MAPE:** ~10.15%
  - **R² Score:** ~86.4%

These results indicate the model can explain a large portion of revenue variance and provides an effective baseline for further improvement.

---

## License

This project is for educational and research purposes.

---

## Acknowledgments

- [Scikit-learn documentation](https://scikit-learn.org/stable/)
- [pandas documentation](https://pandas.pydata.org/)
- Data source: Provided with the project

---

Happy Predicting!