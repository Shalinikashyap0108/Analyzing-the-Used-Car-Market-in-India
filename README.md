# Navigating the Pre-Owned Automotive Landscape with Data-Driven Precision

In an ever-evolving automotive market, determining the true value of a used car is both an art and a science. Pricing can vary dramatically depending on mileage, brand, age, condition, and more—creating complexity for both buyers and sellers. This project leverages a real-world dataset of 5,975 used cars to deliver actionable insights through data cleaning, exploratory analysis, and feature engineering.

Designed with car buyers, dealerships, and data professionals in mind, this analysis aims to uncover the hidden patterns that influence resale prices, ultimately supporting smarter purchasing and pricing strategies.

**Dataset Overview**

The dataset comprises 5,975 records of used cars, each with features essential to assessing market value. These include the car name and model, city of sale, year of manufacture, total kilometers driven, fuel type (e.g., Petrol, Diesel), transmission type (manual or automatic), and number of previous owners. It also covers performance and specification metrics such as mileage (in kmpl or km/kg), engine displacement (cc), horsepower, and seating capacity. The selling price (in INR) is the target variable, while a derived feature, Car_Age, captures the vehicle's age to aid in valuation analysis. Understanding this dataset allows us to pinpoint trends in the used car market, identify anomalies, and make accurate predictions.

**Data Preprocessing**

Before meaningful analysis, the dataset undergoes extensive cleaning to ensure consistency and reliability:

- Missing Value Treatment: Extracted numeric values from text-heavy columns such as Power and Engine.

- Mileage Standardization: Converted mileage values from km/kg to kmpl using a multiplier (1.4) for uniformity.

- Brand Normalization: Standardized brand names (e.g., "ISUZU" to "Isuzu") to prevent redundancy.

- Outlier Detection: Flagged extreme values in mileage, price, and kilometers driven using visual and statistical techniques.

**Exploratory Data Analysis**

With clean data, we explored key trends and anomalies:

- Car Age Distribution: Most vehicles range between 5 to 12 years old, with outliers dating back to 1998.

- Mileage & Price Outliers: Detected unrealistic mileage values and price extremes above ₹160 lakhs, signaling potential entry errors.

- Kilometers Driven: Identified unusually high usage in some cars, requiring normalization or exclusion.

We employed histograms, box plots, and summary statistics to visualize data distributions and assess skewness.

After analyzing the dataset, we segmented the data into budget and luxury car categories based on descriptive statistics and domain insights. For the budget segment, we performed correlation analysis and used the Variance Inflation Factor (VIF) to avoid multicollinearity among features. Then, I focused on predicting the prices of budget cars using both linear and ensemble models. firstly, I trained a Linear Regression model and evaluated it using R², MAE, and MSE. Since, R² score for the linear regression model was low (0.67, i.e. linear model explained only 67% of variation in used car price), I implemented a Random Forest Regressor to improve efficiency, which significantly increased accuracy with an R² score of 0.80 and reduced prediction errors. I also analyzed feature importance to understand which variables (such as Power, Car Age, and Mileage) most influenced price predictions, and the most important feature according to the given set is car age followed power. Which makes sense becasue budget cars arebought by people with limited spending capacity and for them, these two factors matter the most. This model is well-suited for non-linear patterns and provides a more robust solution for budget car price estimation.

**Who Benefits?**

This project offers value across several domains:

- Car Buyers: Understand what drives price variations and make informed purchase decisions.

- Dealerships: Use data-driven insights to optimize inventory pricing and customer targeting.

- Data Analysts & Scientists: Learn real-world techniques for cleaning, transforming, and analyzing complex datasets.
