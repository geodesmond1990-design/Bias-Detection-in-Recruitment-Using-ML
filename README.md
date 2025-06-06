# Bias Detection in Recruitment Using Machine Learning

This project demonstrates how to detect potential bias in recruitment processes using machine learning and fairness metrics.

## Project Overview

We use a recruitment dataset containing features like:
- Gender
- Age
- Education Level
- Experience Years
- Hiring Decision (Hired or Not)

The workflow includes:
1. Preprocessing the data (One-Hot Encoding for categorical features).
2. Training a Random Forest Classifier to predict hiring decisions.
3. Analyzing feature importances to understand key drivers.
4. Detecting bias using:
   - Hiring Rate by Gender
   - Disparate Impact (80% Rule)
   - Statistical Parity Difference (SPD)
5. Exporting the results into an Excel file with multiple sheets.

## Files Generated

- `Bias_Detection_Results_With_Predictions.xlsx` — Excel file containing:
  - **Hiring Rates** by gender
  - **Bias Metrics** summary (Selection Rates, Disparate Impact, SPD)
  - **Feature Importances** (model feature rankings)
  - **Predictions** (actual and predicted hiring decisions)

## How to Use

1. **Prepare Dataset**: Ensure your dataset has the following columns:
    - `gender` (0 = Male, 1 = Female)
    - `age` (numeric)
    - `education_level` (categorical: Bachelors, Masters, PhD, etc.)
    - `experience_years` (numeric)
    - `hired` (0 = Not Hired, 1 = Hired)

2. **Install the required Python libraries**:
```bash
pip install pandas scikit-learn matplotlib openpyxl
```

3. **Run the script**:
- Load your recruitment dataset.
- Run the Python script.
- Check the generated Excel file for the results.

4. **Check the generated Excel file**:
- Open `Bias_Detection_Results_With_Predictions.xlsx`.
- Review the hiring rates, bias metrics, feature importances, and prediction results.

## Key Fairness Metrics

- **Disparate Impact (DI)**: Ratio of selection rates between protected and unprotected groups.
  - DI < 0.8 or DI > 1.25 indicates potential bias (based on the 80% rule).

- **Statistical Parity Difference (SPD)**: Difference in selection rates between protected and unprotected groups.
  - SPD close to 0 indicates fairness.

## Author

© 2025 Okes Imoni
