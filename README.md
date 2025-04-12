# Navigating the Pre-Owned Automotive Landscape with Data-Driven Precision

**Project Overview: From Curiosity to Insight**

This project dives into a real-world dataset of 5,975 used cars sold across India, aiming to reveal the hidden factors that influence their market price. Through comprehensive data cleaning, exploratory analysis, and machine learning modeling, I build predictive insights that support smarter negotiations and pricing strategies.

**Dataset at a Glance**

The dataset includes:

- Car specifications: Year of manufacture, kilometers driven, fuel type, transmission type, engine capacity, power (BHP), mileage, and seating capacity.

- Ownership and transaction details: Number of previous owners, selling city, and selling price (target variable).

- Derived features: Notably, I created Car_Age to better represent the impact of vehicle age on depreciation and value.

**Data Preprocessing: Cleaning the Road Ahead**

Before diving into modeling, the dataset was meticulously cleaned and standardized:

- Missing Value Treatment: Extracted numerical values from text-heavy columns like "Power" and "Engine."

- Mileage Standardization: Normalized different units (e.g., km/kg converted to kmpl using a 1.4x multiplier).

- Brand Harmonization: Standardized brand names to ensure grouping consistency.

- Outlier Detection: Visual and statistical techniques flagged anomalies in mileage, price, and kilometers driven.

These steps ensured a solid foundation for analysis and modeling.

**Exploratory Data Analysis: Trends That Tell Stories**

With a cleaned dataset, I began exploring key questions:

- How old are most used cars? Majority range between 5 to 12 years, with rare outliers dating back to 1998.

- Any data errors? Mileage values up to 47 kmpl and prices exceeding ₹1.6 crore revealed presence of outliers, which were later addressed.

- How far do used cars typically go? Kilometers driven varied widely, influencing depreciation and resale value.

Visualizations like histograms, boxplots, and correlation matrices helped identify influential features and eliminate noise.

**Segmenting the Market: Budget vs. Luxury Cars**

To provide more relevant insights, the dataset was split into budget and luxury car segments based on price distribution and domain understanding. This helped tailor models to the unique patterns in each segment.

The initial focus was on budget cars, where purchasing decisions are highly sensitive to price, age, and performance trade-offs.

**Building the Model: Predicting Budget Car Prices**

I began with a Linear Regression model to capture basic trends. The results showed:

- R² Score: 0.67 (67% of variance in price explained)

- MAE: ~₹91,000

- MSE: 1.28

While informative, the linear model didn’t fully capture non-linear patterns in the data.

To improve performance, I implemented a Random Forest Regressor, which significantly enhanced results:

- R² Score: 0.80

- MAE: ~₹67,000

- MSE: 0.78

The Random Forest model also provided feature importance, identifying Car_Age, Power, and Mileage as the top predictors—exactly the features I debated about before starting this project. It reaffirmed that age and engine performance are key determinants for price in the budget segment—especially for buyers with limited spending flexibility.

**Multicollinearity & Model Diagnostics**

To ensure robustness:

Correlation Analysis and Variance Inflation Factor (VIF) were used to detect multicollinearity. Power and Engine had a high correlation (0.81), but both were retained due to VIF scores below the critical threshold (VIF < 5), confirming acceptable levels of redundancy. I also performed OLS Regression using statsmodels to examine feature significance with p-values and confidence intervals.

**Key Takeaways**

- Budget car prices are most influenced by Car Age, Power, and Mileage.

- Random Forest outperforms linear models in predicting non-linear relationships in used car pricing.

- Data supports what buyers intuitively know—but quantifies it, making price negotiation smarter and more evidence-based.

**Who Can Use This?**

This project provides real value to:

- Car Buyers: Get a fair estimate of car value before negotiating.

- Dealerships: Use insights to price inventory more competitively.

- Data Enthusiasts & Analysts: Learn how to clean, analyze, and model real-world messy data in a meaningful domain.

**What's Next?**

Stay tuned for modeling on the luxury segment, where brand value, transmission type, and fuel category might play a stronger role. I also plan to deploy this model as a simple web app to help users estimate resale value instantly.
