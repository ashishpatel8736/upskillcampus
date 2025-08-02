# Smart City Traffic Patterns

This project analyzes and predicts traffic flow patterns at city junctions using data science and machine learning techniques. It is focused on understanding urban traffic behavior and forecasting vehicle counts to support smarter city planning and traffic management.

## Overview

- **Data Source:** Hourly vehicle counts at various city junctions, split into training and test sets in CSV format.
- **Goal:** Build a predictive model to estimate the number of vehicles at different times and junctions.

## Workflow

1. **Data Loading:**
   - Load `train.csv` and `test.csv` datasets with timestamps and junction information.
2. **Feature Engineering:**
   - Extract time-based features from the `DateTime` column:
     - Hour
     - Day
     - Month
     - Weekday
     - Weekend indicator
3. **Model Training:**
   - Use the engineered features to train an XGBoost regression model (`XGBRegressor`) to predict vehicle counts.
   - Split training data further for validation.
4. **Evaluation:**
   - Evaluate the model using Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE).
   - Plot actual vs. predicted vehicle counts for visual comparison.
5. **Prediction & Submission:**
   - Predict vehicle counts for the test set.
   - Save predictions in `final_submission.csv`.

## Key Code Steps

- **Libraries:** pandas, numpy, matplotlib, sklearn, xgboost
- **Feature Engineering Function:** Adds hour, day, month, weekday, and is_weekend columns for better temporal modeling.
- **Model:** XGBoost regressor with standard hyperparameters (`n_estimators=100`, `max_depth=6`, `learning_rate=0.1`).
- **Validation:** Uses an 80/20 train-validation split.
- **Metrics:** Reports MAE and RMSE for regression performance.
- **Visualization:** Plots first 100 samples of actual vs. predicted values.

## Example Output

- **Final MAE:** ~6.41
- **Final RMSE:** ~9.66

## File Structure

- `Smart_city_traffic_patterns/smart_city_traffic_patterns.ipynb`: Main notebook with all code and analysis.
- `train.csv`, `test.csv`: Input datasets.
- `final_submission.csv`: Output predictions.

## Usage

1. Ensure all required libraries are installed.
2. Run the notebook `smart_city_traffic_patterns.ipynb` from the `Smart_city_traffic_patterns` directory.
3. Review plots and output files for results.

## License

This project is for educational and research purposes.
