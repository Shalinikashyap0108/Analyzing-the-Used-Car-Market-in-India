# Unlocking Insights: The Story of Used Car Data Analysis

In today's fast-paced automobile market, buyers and sellers face a common challenge—how to determine the true value of a used car? Prices can vary drastically based on factors like mileage, brand, and condition, making it difficult to make informed decisions. This project embarks on a journey to analyze a dataset of used cars, applying data cleaning, exploratory analysis, and feature engineering to uncover valuable insights. This analysis is especially helpful for car dealers, buyers, and data enthusiasts looking to understand the factors that influence a car’s resale price. By refining and transforming raw data, we pave the way for smarter purchasing and pricing strategies.

The dataset contains details of 5,975 used cars, each with key attributes that shape their market value. These include:
- Name: Car name
- Location: City where the car is available
- Year: Year of manufacture
- Kilometers_Driven: Total distance driven
- Fuel_Type: Type of fuel used
- Transmission: Manual or automatic
- Owner_Type: Number of previous owners
- Mileage: Efficiency in kmpl or km/kg
- Engine: Displacement in cc
- Power: Horsepower of the car
- Seats: Seating capacity
- Price: Selling price of the car
- Car_Age: Derived feature for vehicle longevity

Understanding this dataset allows us to pinpoint trends in the used car market, identify anomalies, and make accurate predictions.

Before diving into analysis, we must refine the dataset by:

- Handling Missing Values: Extracting numerical values from text-based columns like Power and Engine to ensure consistency.

- Standardizing Mileage Data: Converting mileage from km/kg to kmpl using a standard multiplier (1.4) for accurate comparisons.

- Correcting Data Entries: Standardizing brand names (e.g., ISUZU to Isuzu) to eliminate inconsistencies.

These steps ensure we work with clean, reliable data, laying the foundation for meaningful insights. Once cleaned, the data reveals fascinating insights:

- Car Age Distribution: Most cars are between 5-12 years old, with the oldest dating back to 1998.

- Mileage Anomalies: Some cars have unrealistic mileage values, indicating possible data entry errors.

- Price Outliers: Certain listings exceed 160K, hinting at anomalies that require further investigation.

- Kilometers Driven: Some vehicles have extremely high mileage, suggesting the presence of outliers that need transformation.

Using histograms and boxplots, we detect skewness and anomalies, ensuring our data is fit for predictive modeling.

Transforming Data: The Power of Feature Engineering

To improve accuracy, we introduce:

Log Transformation: Reducing skewness in variables like Kilometers_Driven and Price.

Derived Features: New indicators such as Price_per_HP (price per unit of horsepower) and Fuel_Efficiency to enhance our analysis.

Luxury Indicator: Classifying cars based on brand and horsepower to distinguish economy from premium models.

These enhancements refine our dataset, making it more useful for predictive modeling and pricing analysis.

The Impact: Who Benefits from This Analysis?

Car Buyers: Gain clarity on what features matter most in pricing.

Dealerships: Optimize pricing strategies based on data-driven insights.

Data Scientists: Learn best practices in data cleaning, transformation, and analysis.

By applying structured data analysis, we create a robust dataset that helps make informed automotive decisions.

How to Use This Project

Clone the repository.

Run the Jupyter Notebook to explore the data.

Follow the steps to clean, transform, and analyze the dataset.

License

This project is open-source and free to use. Drive smarter with data! 🚗💡
