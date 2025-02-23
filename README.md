# Airbnb Boston Listings Analysis

## Overview

This project analyzes Airbnb listings in Boston to understand key factors influencing demand, performance, and pricing. The analysis follows the **CRISP-DM (Cross-Industry Standard Process for Data Mining)** framework, which includes six phases:

1. **Business Understanding**
2. **Data Understanding**
3. **Data Preparation**
4. **Modeling**
5. **Evaluation**
6. **Deployment**

The goal is to provide actionable insights for hosts, travelers, and stakeholders in the Airbnb ecosystem.

---

## Business Understanding

The analysis addresses three key questions:

1. **Demand**: Which neighborhoods have the highest and lowest demand based on availability and reviews?
2. **Performance**: What characteristics do top-rated listings share?
3. **Pricing**: What factors influence the price of an Airbnb listing in Boston?

---

## Data Understanding

The dataset used is `listings.csv`, which contains 3,585 rows and 95 columns. Key steps in this phase include:

- Inspecting missing values, data types, and distributions.
- Identifying columns with high null values and dropping those with more than 75% null values.
- Cleaning and transforming data types for columns like `price`, `host_response_rate`, and `host_acceptance_rate`.

---

## Data Preparation

### Key Steps:
1. **Dropping Columns**: Columns with more than 75% null values were removed.
2. **Handling Null Values**: Null values in `beds`, `bedrooms`, and `bathrooms` were filled with their median values.
3. **Data Type Conversion**: Columns like `price`, `host_response_rate`, and `host_acceptance_rate` were cleaned and converted to numeric types.
4. **Categorical Variables**: Dummy variables were created for categorical columns like `property_type`, `room_type`, and `bed_type`.
5. **Feature Engineering**: A new feature, `amenities_count`, was created to count the number of amenities offered by each listing.

---

## Modeling

### Key Steps:
1. **Dummy Variables**: Created for categorical features like `property_type`, `room_type`, and `bed_type`.
2. **Handling Host Response Time**: Converted `host_response_time` into numeric values based on response speed.
3. **Binary Encoding**: Columns with "t" and "f" values were converted to 1 and 0, respectively.
4. **Linear Regression**: Used to model the relationship between listing features and price.

---

## Evaluation

### 1. **Demand Analysis**
- **Top Neighborhoods**: Jamaica Plain, Leather District, and Longwood Medical Area have the highest demand.
- **Lowest Demand Areas**: West End, Mattapan, and Chinatown have the lowest demand.
- **Key Insights**: High-demand neighborhoods have limited availability and better reviews, while low-demand areas need improvements in quality or marketing.

### 2. **Performance Analysis**
- **Top-Rated Listings**: Characterized by superhosts, higher host responsiveness, more amenities, and greater guest engagement.
- **Key Insights**: Price and size don’t significantly impact ratings, but lower availability indicates higher demand.

### 3. **Pricing Analysis**
- **Linear Regression Model**: Achieved an R² score of 0.690, explaining 69% of the variance in price.
- **Key Insights**: The model performs well in terms of explanatory power but has room for improvement in prediction accuracy.

---

## Deployment

### Deliverables:
1. **GitHub Repository**: Contains the code, data, and documentation for the analysis. [Link to GitHub Repo](https://github.com/scknylmz/Airbnb_Boston_Analysis)
2. **Blog Post**: A non-technical summary of the findings, aimed at a general audience. [Medium](https://medium.com/@scknylmz35/unlocking-the-secrets-of-airbnb-listings-in-boston-a-data-driven-guide-for-hosts-and-travelers-f5d42f6803a6)

---

## Tools and Libraries Used

- **Python**: Primary programming language.
- **Pandas**: Data manipulation and analysis.
- **NumPy**: Numerical computations.
- **Matplotlib & Seaborn**: Data visualization.
- **Scikit-learn**: Machine learning modeling and evaluation.
- **Statsmodels**: Statistical modeling.


## Future Work

- **Outlier Handling**: Investigate and address outliers to improve model accuracy.
- **Non-Linear Models**: Explore advanced models like decision trees, random forests, or gradient boosting.
- **Feature Engineering**: Create additional features to capture more nuanced relationships in the data.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Contact

For questions or feedback, please reach out to Seckin Yilmaz at [scknylmz@yahoo.com].
