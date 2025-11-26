#HR Attrition Analysis — Predicting & Preventing Employee Turnover

#Business Problem
> "Why are employees leaving? Can we predict attrition early and target retention efforts?"

## Data Science Approach
1. **Convert to binary classification**: `Attrition = Yes/No`
2. **Three models for robustness & insight**:
   - **Logistic Regression**: Interpretable odds ratios (HR-friendly)
   - **Random Forest**: Captures non-linear patterns (e.g., `JobSatisfaction × Overtime`)
   - **XGBoost + SHAP**: State-of-the-art prediction + explainable AI

## Key Insights (From Results)
- **Model performance**:
  - Random Forest AUC: **0.811** → Strong predictive power
  - Logistic Regression: **0.805** → strong predictive power 
  - XGBoost AUC: **0.779** → Slightly lower but more interpretable via SHAP
- **Top 3 global drivers of attrition (SHAP)**:
  1. `OverTime` — Highest impact (mean |SHAP| = 0.62)
  2. `MonthlyIncome` — Second highest (0.44)
  3. `StockOptionLevel` — Third (0.38)
- **Actionable insight**: Employees working overtime with low income or stock options are at highest risk.

## How to Run (100% Reproducible on Windows)

### Prerequisites
- Windows 10/11  
- **Anaconda 2023.09 or later** (includes Python 3.11.5)  
  → [Download Anaconda (64-bit)](https://repo.anaconda.com/archive/Anaconda3-2023.09-0-Windows-x86_64.exe)  
  →  During install: **Check “Add to PATH”** and **“Register Anaconda”**

### Steps
1. **Clone this repo**  
   Open **Anaconda Prompt** (search in Start menu) and run:
   ```powershell
   git clone https://github.com/albertogoga/hr-attrition-analysis.git
   cd hr-attrition-analysis
