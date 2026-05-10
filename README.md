# DJIA Smart-Beta Allocation with Machine Learning

This project develops a **Smart-Beta** investment framework applied to the components of the **Dow Jones Industrial Average (DJIA)** for the 2007-2026 period. The goal is to outperform the reference benchmark (DJITR) using signals derived from fundamental metrics and supervised learning models.

## 📈 Project Overview
The workflow is divided into three main phases:
1. **Data Engineering**: Extraction of historical data (adjusted prices and monthly fundamentals) via Yahoo Finance and FRED.
2. **Benchmark Reconstruction**: Accurate reconstruction of the Total Return Index (DJITR) to ensure a "fair" comparison (including reinvested dividends).
3. **ML Modeling**: Implementation and comparison of regularized linear models (Ridge, Lasso) and non-linear models (Random Forest, XGBoost) using a walk-forward approach.

## 📂 File Structure (Suggested Order)

1. **[01_Dataset_Building.ipynb](./01_Dataset_Building.ipynb)** Panel dataset construction. Includes the calculation of fundamental ratios (P/E, P/B, ROE, Debt/Equity) and the integration of macroeconomic variables (VIX, Yield Curve).
   
2. **[02_Benchmark_Reconstruction.ipynb](./02_Benchmark_Reconstruction.ipynb)** "Chain-linking" procedure to reconstruct the historical performance of the DJIA including dividends.
   
3. **[03_Model_Comparison.ipynb](./03_Model_Comparison.ipynb)** The analytical core: model training and Out-of-Sample (OOS) evaluation. Comparison between the stability of linear models vs. the complexity of XGBoost/RF.

4. **[Final_Presentation.pdf](./AIBF_Final_Presentation.pdf)** Final report featuring Equity Curve plots, Drawdown analysis, and performance scorecards.

## 🏆 Key Results
* **Winning Model**: The **Ridge + Lasso** ensemble showed the highest OOS robustness.
* **Performance**: Generated an **annual Alpha of approximately 0.81%** relative to the DJITR benchmark, with superior risk management (improved Sharpe Ratio).
* **Target**: Prediction of monthly excess returns for dynamic portfolio rebalancing.

---
**Authors**: Leonardo Alosi, Samuele Flaiban, Giulio Gottardi, Camilla Pilone  
**Course**: Artificial Intelligence for Banking & Finance (Prof. Lagasio)  
**Date**: May 2026
