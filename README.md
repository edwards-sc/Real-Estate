# Real-Estate Investment Decisions: Identifying Favorable Markets
# Milestone 2: Real Estate Investment Decisions: Identify Favorable Markets with Rental Demand
## Three separate datasets were acquired from Zillow:
1. **Zillow Observed Rental Index (ZORDI)**: Tracks trends in rental prices over time, highlighting regions with strong rental demand.
2. **Sales Count Nowcast**: Sales data provide insights into real estate market trends, including average sales prices and transaction volumes, to gauge market favorability for buyers.
3. **Market Heat Index (MHI)**: Evaluates the balance of supply and demand in real estate markets, offering a measure of how seller- or buyer-favorable a market is.

## Data Preparation
Duplicates were checked and removed, data frames were merged on common columns and dates to create a unified dataset. Dates were aligned across all datasets to maintain consistency in trend analysis. Features created for the model include Ave_Rental_Yield, Yield_Growth, Yield_Variance.

## Methods
- **Random Forest Regressor**: Applied to the updated data frame with the target set as Avg_Rental_Yield. Performance: Mean Square Error (MSE) at 0.887, and R2 Score at 0.999. The Cross-Validation Score at -0.84 indicates possible overfitting.
- **Hyperparameter Optimization with Grid Search**: Addressed overfitting. Performance: MSE at 0.96 and R2 Score at 0.999. Cross-Validation Score at -0.84, indicating overfitting.
- **Ensemble Model (Random Forest Regressor and XGBoost)**: Applied to reduce overfitting. Performance: MSE at 0.728 and R2 Score at 0.999. Cross-Validation Score at -0.657.

## Analysis
All models achieved high R2 Scores and low MSE values. Negative Cross-Validation Scores for Random Forest and Grid Search suggest overfitting. The Ensemble model improved Cross-Validation Score and reduced overfitting. Figure 1 demonstrated Ensemble model’s predicted values, reinforcing the model’s accuracy and fit.
