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

📌 **Next Deliverables:**
- Full Jupyter Notebooks with cleaned code, EDA, and modeling steps.
- GitHub repository with all files (including this README).

Jupyter notebook link: 
