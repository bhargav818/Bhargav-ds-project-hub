# COVID-19 Data Analysis & Prediction Project

This project analyzes and visualizes the spread and recovery trends of COVID-19 using real patient data and applies machine learning (time series forecasting) to predict the number of cases in the near future. The approach leverages Python, pandas, Plotly, and Facebook Prophet to deliver interactive insights.

---

## 📊 Problem Statement

Given time-series data about COVID-19 patients, the goals are to:

- Visualize the impact and analyze trends of infection and recovery rates.
- Predict the number of cases expected a week into the future based on current trends.

---

## 🛠️ Technologies & Libraries Used

- **Python**: Core programming language.
- **pandas**: Data manipulation and analysis.
- **NumPy**: Numerical operations.
- **Matplotlib & Seaborn**: Basic data visualization.
- **Plotly**: Interactive and advanced visualization.
- **Facebook Prophet**: Time series forecasting for future prediction.
- **Jupyter Notebook**: Interactive development and reporting.

---

## 📁 Project Structure

- `COVID 19 Project.ipynb`: Main Jupyter notebook for data exploration, visualization, and modeling.
- `covid_19_clean_complete.csv`: The cleaned dataset containing daily COVID-19 statistics by country and region.

---

## 📝 How to Run

1. **Clone the Repository**
   ```bash
   git clone <repo-url>
   cd <repo>
   ```

2. **Install Dependencies**
   - It's recommended to use a virtual environment.
   - Required packages: `pandas`, `numpy`, `matplotlib`, `seaborn`, `plotly`, `prophet`, `jupyter`
   - Install via pip:
     ```bash
     pip install pandas numpy matplotlib seaborn plotly prophet jupyter
     ```

3. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook
   ```
   - Open `COVID 19 Project.ipynb` in your browser and follow the cells.

---

## 🧾 Features & Workflow

1. **Data Loading & Cleaning**
   - Loads COVID-19 data and checks for missing values/duplicates.
   - Explores the columns: country, region, date, confirmed, deaths, recovered, active, etc.

2. **Exploratory Data Analysis (EDA)**
   - Overview of missing values, unique countries, and regional distributions.
   - Country-wise and region-wise aggregations.

3. **Visualization**
   - Interactive and static plots (using Matplotlib and Plotly) for:
     - Time-series of confirmed, deaths, recovered, and active cases.
     - Top-affected countries and regions.
     - Trends over time for specific countries (e.g., India).
     - Comparison of cases, deaths, and recoveries by region/country.

4. **Forecasting with Facebook Prophet**
   - Prepares the time series data for Prophet.
   - Builds and fits the forecasting model.
   - Predicts future COVID-19 cases (up to a week ahead).
   - Plots predicted vs. actual trends.

---

## 📈 Example Outputs

- Daily confirmed cases and trends.
- Country-wise total deaths and recoveries.
- Interactive predictions for future case counts.

---

## 🧠 Insights

- The analysis provides a clear overview of the pandemic's evolution.
- Forecasting helps anticipate healthcare needs and policy decisions.

---

## 💡 How to Contribute

1. Fork the repo and clone your fork.
2. Create a new branch for your feature or bug fix.
3. Commit your changes and create a pull request.

---

## 🙏 Acknowledgements

- [Johns Hopkins University COVID-19 Data Repository](https://github.com/CSSEGISandData/COVID-19)
- [Facebook Prophet](https://facebook.github.io/prophet/)
- [Plotly](https://plotly.com/)

---

## 📄 License

This project is for educational and research purposes. Please check the dataset's licensing before commercial use.

---