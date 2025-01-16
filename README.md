# README for XYZ Subscription Prediction Project

## Overview
This project focuses on predicting which users of the music-listening social networking site "XYZ" are most likely to convert from free users to premium subscribers within six months, based on a targeted marketing campaign. Using a dataset of user activity and demographics, we applied various machine learning techniques to identify high-potential adopters and optimize XYZ’s marketing strategy.

## Files in Repository
- **Dataset.csv**: The dataset containing user activity, demographics, and campaign results.
- **Technical_Report.pdf**: The technical report detailing the analytical process, modeling techniques, and performance evaluation.
- **Presentation.mp4**: A 5-minute video presentation summarizing the project for a managerial audience.
- **analysis_script.Rmd**: RMarkdown script for data preprocessing, EDA, feature engineering, modeling, and performance evaluation.

## Key Components
1. **Data Preparation**:
   - Preprocessed the dataset by converting categorical columns to factors.
   - Split the data into 80% training and 20% testing folds.
   - Addressed class imbalance using oversampling and undersampling with the `ovun.sample` method.

2. **Exploratory Data Analysis**:
   - Visualized data distributions using boxplots.
   - Investigated outliers and feature importance.

3. **Modeling and Evaluation**:
   - Tested multiple models including:
     - K-Nearest Neighbors (KNN)
     - Decision Trees
     - Naive Bayes
   - Selected **Decision Tree** as the final model based on high recall, AUC, and F1-score.
   - Used cross-validation for robust performance evaluation.

4. **Performance Metrics**:
   - **Recall**: Priority metric to ensure maximum capture of potential adopters.
   - **AUC-ROC**: Evaluated model's ability to distinguish between adopters and non-adopters.
   - **F1-Score**: Balanced precision and recall for overall performance assessment.

5. **Threshold Tuning**:
   - Adjusted prediction thresholds to optimize marketing targeting based on budget and campaign goals.

6. **Lift Curve Analysis**:
   - Demonstrated how targeting the top 25% of predicted adopters doubles the likelihood of conversions, maximizing ROI for the marketing campaign.

## Insights
- Decision Trees proved to be the most effective for this task due to their ability to handle feature importance automatically and robustly classify users despite class imbalance.
- Targeting based on model predictions improves campaign efficiency by focusing on users with the highest likelihood of conversion.

## Future Work
- Experiment with ensemble methods like Random Forests or Gradient Boosting for potentially higher performance.
- Incorporate additional user behavioral metrics or external data for improved predictions.
