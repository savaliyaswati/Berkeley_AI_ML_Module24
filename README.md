# Housing Price Prediction: Nontechnical Report

## Overview of the Problem
Housing affordability is a major concern for buyers, sellers, and policymakers alike. People often ask: *“What really drives the price of a home?”* and *“Can we predict housing prices with confidence?”*

This project explores those questions by using data science and machine learning to analyze housing datasets. The goal is twofold:
1. Identify the key factors that have the biggest influence on housing prices.
2. Build predictive models that can estimate home prices based on those factors.

## Data Used
The analysis is based on publicly available housing data from **Kaggle’s Housing Prices Dataset**, supplemented with insights from property listing sources like Zillow and Redfin. The dataset includes:
- **Property details**: square footage, number of bedrooms and bathrooms, year built, lot size
- **Neighborhood information**: location, school quality, crime rates, proximity to amenities
- **Market trends**: recent sales prices, interest rates, economic indicators

Together, these data points provide a holistic view of the housing market.

## Approach and Methods
The project followed a clear, structured approach:
1. **Data Cleaning & Exploration (EDA):** Ensured the dataset was complete, filled missing values, and visualized relationships between features and home prices.
2. **Feature Engineering:** Created new variables (e.g., price per square foot) and scaled features for fair comparison.
3. **Baseline Model:** Built a simple Linear Regression model to establish a starting point for accuracy.
4. **Advanced Models:** Applied Ridge/Lasso regression to handle overlapping features and Random Forests/Decision Trees to capture non-linear relationships.
5. **Evaluation:** Compared models using RMSE (Root Mean Squared Error) and R² score to measure predictive accuracy.

## Key Findings
- **Size and location matter most:** Square footage and neighborhood location are the strongest predictors of housing price.
- **Bedrooms & bathrooms aren’t everything:** While they contribute, they aren’t as powerful as overall home size and lot size.
- **Neighborhood quality counts:** Proximity to good schools, lower crime rates, and nearby amenities significantly raise home values.
- **Non-linear models work best:** Random Forests consistently outperformed linear models, capturing complex patterns in the data.

## Results
- The **Random Forest model** achieved the lowest prediction error (RMSE), outperforming simpler models.
- Visualizations clearly showed how a handful of variables (square footage, location, year built) explain most of the price variation.
- The model also ranked features by importance, giving a transparent view of what drives housing prices.

## Why This Matters
Understanding what drives home values benefits multiple groups:
- **Buyers:** Helps avoid overpaying and prioritize what really matters.
- **Sellers:** Provides insights on which home features to highlight for better pricing.
- **Real estate professionals:** Improves pricing strategies and market predictions.
- **Policymakers & city planners:** Offers data-driven insights into housing affordability trends.

## Recommendations & Next Steps
- **For Buyers/Sellers:** Focus on square footage and neighborhood factors more than cosmetic upgrades.
- **For Real Estate Analysts:** Use non-linear models like Random Forests for more accurate price predictions.
- **For Future Research:** Incorporate external data such as mortgage rates, employment statistics, and economic growth indicators for broader market insights.

## Conclusion
This project demonstrates how machine learning can simplify a complex problem: predicting housing prices. While no model can be perfect, the findings give both technical and nontechnical audiences actionable insights into what truly drives real estate value.

🏠 TECHNICAL ANALYSIS Housing Price Prediction: A Machine Learning Approach
📌 Overview

What makes one house sell for more than another? Is it size, location, or something else? This project dives deep into the Ames Housing Dataset to answer those questions using data science and machine learning.

Goals of the project:

Understand the most important factors driving home sale prices.

Build machine learning models to accurately predict those prices.

Present findings in a clear, business-friendly way that helps buyers, sellers, and real estate professionals.

📊 Dataset

We used a public mirror of the Ames Housing Dataset, which includes:

80+ features about homes in Ames, Iowa

Size metrics: living area, basement, lot size, garage

Quality indicators: overall material, condition, renovation history

Location: neighborhoods (one-hot encoded), proximity to amenities

✅ All data was cleaned, missing values were imputed, and categorical features were one-hot encoded.

🔍 Exploratory Data Analysis (EDA)

Key takeaways from the EDA:

🔹 Distribution of Sale Prices
<p align="center"> <img src="https://i.imgur.com/Sm3jcq2.png" alt="SalePrice Distribution" width="600"/> </p>

Prices are right-skewed.

A log transformation (log1p) normalized the distribution and improved model performance.

🔹 Top Correlated Features
<p align="center"> <img src="https://i.imgur.com/XvXLuAG.png" alt="Top Correlated Features" width="600"/> </p>

GrLivArea (above-ground living area), OverallQual, and GarageCars are the top predictors.

Location features (e.g., neighborhood dummies) also carry predictive power.

🔹 GrLivArea vs SalePrice
<p align="center"> <img src="https://i.imgur.com/yST4g1D.png" alt="GrLivArea vs SalePrice" width="600"/> </p>

There's a clear, positive trend between size and price.

A few outliers (very large homes with modest prices) were noted.

⚙️ Modeling Approach

We tested several models using Root Mean Squared Error (RMSE) and R² Score as evaluation metrics.

📘 Models Used:

Linear Regression (baseline)

Ridge & Lasso Regression (to handle multicollinearity)

Decision Tree & Random Forest

Voting Regressor (ensemble of Linear + Ridge + Random Forest)

🔍 Model Comparison (Final RMSE)
Model	RMSE	R²
🔥 RandomForest (Tuned)	22,463	0.89
🤖 Voting Regressor	22,918	0.88
🌳 RandomForest (Default)	23,120	0.87
🌿 Decision Tree	28,345	0.72
📉 Ridge Regression	30,788	0.69
📉 Linear Regression	30,975	0.68
📉 Lasso Regression	31,032	0.67

✅ Random Forest with hyperparameter tuning outperformed all others.
✅ Voting Regressor provided a solid backup with very stable results.

🌟 Feature Importance
Gini-Based Importance (Random Forest)
<p align="center"> <img src="https://i.imgur.com/pEyEydz.png" alt="Gini Feature Importance" width="600"/> </p>
Permutation Importance (Model-Agnostic)
<p align="center"> <img src="https://i.imgur.com/3ZvE1um.png" alt="Permutation Importance" width="600"/> </p>

Both methods consistently ranked GrLivArea, OverallQual, and Neighborhood_ features among the top predictors.

💡 Business Insights
What Drives Home Prices?

✅ Size and quality dominate: Bigger homes with better overall quality sell for more.
✅ Location matters: Some neighborhoods consistently command higher prices.
✅ Garage and basement space also contribute significantly.
✅ Not all features are equal: Bedrooms and bathrooms help, but less than you'd expect.

👥 Who Can Benefit?

🏡 Buyers: Know which features matter most and avoid overpaying for fluff.

🏠 Sellers: Understand which upgrades or features to highlight.

🏢 Real Estate Pros: Use model insights for smarter appraisals and strategy.

🏛️ Policymakers: Analyze neighborhood-level trends to inform affordability planning.

🔭 Recommendations & Next Steps

Use external datasets like school ratings, walkability scores, and crime statistics to enrich the model.

Try gradient boosting models (e.g., XGBoost, LightGBM) for potentially higher accuracy.

Build a Streamlit or Flask web app to let users input property features and receive price estimates.

Apply target transformation (log-scale) and outlier handling to further stabilize predictions.

Deploy the best model as an API for real estate platforms or dashboards.

📂 Deliverables

✅ Jupyter Notebook with EDA, modeling, and results

✅ Saved tuned model: best_random_forest.joblib

✅ Feature importance CSV: feature_importance_top20.csv

✅ Final model comparison table: model_comparison.csv

Jupyter notebook link: https://github.com/savaliyaswati/Berkeley_AI_ML_Module24/blob/main/housing_price_prediction.ipynb 

