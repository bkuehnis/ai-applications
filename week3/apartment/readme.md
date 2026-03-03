# Model Iterations Documentation  
## Task: Apartment Price Prediction (Regression)

---

## Summary of Iterative Process

| Iteration | Objective | Key Changes | Models Used | CV Mean R² | CV Std Dev | Change in Performance | Fit Diagnosis |
|------------|------------|-------------|-------------|------------|------------|-----------------------|----------------|
| **1** | Build baseline model | - Basic cleaning<br>- Missing value imputation<br>- One-hot encoding<br>- Standard scaling<br>- 5-fold CV | Linear Regression<br>Random Forest (n_estimators=100) | 0.78 (RF)<br>0.72 (LR) | 0.06 | Baseline | ☑ Overfitting ☐ Underfitting ☐ Good Fit |
| **2** | Improve generalization | - Feature engineering<br>- Removed correlated features<br>- Log transform target<br>- Hyperparameter tuning<br>- 5-fold CV | Ridge (alpha=1.0)<br>Tuned Random Forest (n_estimators=300, max_depth=15) | 0.86 (RF)<br>0.82 (Ridge) | 0.03 | +0.08 improvement | ☐ Overfitting ☐ Underfitting ☑ Good Fit |

---

## Notes

**Metric:** R², RMSE or other (5-Fold Cross-Validation)

**Created Features:**  
- Apartment Age  
- Total Rooms  
- Price per m²  
- Distance to Center  
- Floor Ratio  

**Final Selected Features:**  
- Living Area  
- Location  
- Apartment Age  
- Total Rooms  
- Distance to Center  
- Floor Ratio  
- Condition  

**Reason for Selection:**  
Chosen based on feature importance, correlation analysis, and cross-validation performance.