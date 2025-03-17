# Media Mix Model (MMM)

## Overview
This project implements a **Media Mix Model (MMM)** using **Python** to analyse the impact of various media channels on total investment. It applies:
- **Adstock Transformation** (carryover effects of media spend)
- **Diminishing Returns** (log transformation)
- **OLS Regression** to estimate media effectiveness
- **Budget Optimization Scenarios**

## Data Used
- **Total Investment**: The dependent variable (target).
- **Media Channels**:
  - TV, Digital, Sponsorship, Content Marketing, Online Marketing, Affiliates, SEM.
- **Time Period**: Monthly data.

## Installation
1. Install required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn statsmodels scikit-learn
   ```
2. Clone this repository:
   ```bash
   git clone https://github.com/Joshua-M/MediaMixModel.git
   ```
3. Navigate to the project directory:
   ```bash
   cd MediaMixModel
   ```
4. Ensure `MediaInvestment.csv` is placed in the project folder.

## Running the Model
Execute the script in a Jupyter Notebook or Python environment:
```bash
python media_mix_model.py
```

## Features
✅ **Exploratory Data Analysis (EDA)**: Trends & Correlations
✅ **Adstock Transformation**: Models delayed media impact
✅ **Diminishing Returns**: Log transformation for realistic media effects
✅ **OLS Regression Model**: Determines media effectiveness
✅ **Budget Scenario Simulation**: Predicts impact of different media allocations

## Model Performance
- **R²:** 90.6% (Model explains 90.6% of variance in Total Investment)
- **MAE:** 10.05
- **RMSE:** 13.06

## Example: Budget Optimization
You can modify media budgets and predict total investment:
```python
new_budget = {
    'TV_log': np.log1p(10),
    'Digital_log': np.log1p(15),
    'Sponsorship_log': np.log1p(5),
    'Content Marketing_log': np.log1p(3),
    'Online marketing_log': np.log1p(7),
    'Affiliates_log': np.log1p(2),
    'SEM_log': np.log1p(8)
}

predicted_investment = predict_investment(new_budget)
print(f"Predicted Total Investment: {predicted_investment:.2f}")
```

## Next Steps
🔹 **Optimize Budget Allocation** (Find the best media mix)
🔹 **Use Bayesian Regression** for uncertainty estimation
🔹 **Expand dataset** with more historical data

## Contributing
Feel free to submit pull requests for improvements!

## License
This project is open-source under the **MIT License**.

