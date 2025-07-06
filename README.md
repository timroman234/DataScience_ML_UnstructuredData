
### Customer Personality Segmentation Project

#### Business Context

Understanding customer personality and behavior is crucial for businesses to enhance satisfaction and increase revenue. This project analyzes customer data from a leading retail company to identify distinct segments based on demographics, personality traits, and purchasing behaviors. Key goals include developing personalized marketing campaigns, improving customer retention, and optimizing resource allocation like inventory management and pricing strategies.

#### Objective

- **Develop personalized marketing campaigns** to boost conversion rates
- **Create retention strategies** for high-value customers
- **Optimize resource allocation** including inventory and pricing
- **Segment customers** using machine learning to uncover actionable insights


### Data Dictionary

#### Customer Information

- `Education`: Customer's education level (e.g., Graduation, PhD)
- `Marital_Status`: Relationship status (e.g., Single, Married)
- `Age`: Approximate customer age
- `Income`: Yearly household income (USD)
- `Kidhome`/`Teenhome`: Number of children/teenagers in household
- `Dt_Customer`: Date of enrollment
- `Recency`: Days since last purchase
- `Complain`: Complaint in last 2 years (1=Yes, 0=No)


#### Spending (Last 2 Years)

- `MntWines`, `MntFruits`, `MntMeatProducts`, `MntFishProducts`, `MntSweetProducts`, `MntGoldProds`: Amount spent per category


#### Purchase Behavior

- `NumDealsPurchases`: Purchases made with discounts
- `NumWebPurchases`/`NumCatalogPurchases`/`NumStorePurchases`: Online/catalog/in-store purchases
- `NumWebVisitsMonth`: Monthly website visits


#### Campaign Response

- `AcceptedCmp1-5`/`Response`: Campaign response (1=Accepted, 0=Declined)


### Methodology

1. **Data Preprocessing**
    - Handled missing values (income filled with median)
    - Removed duplicates and outliers (e.g., extreme income values)
    - Engineered features (converted `Year_Birth` to `Age`)
    - Dropped irrelevant columns (`ID`, `Z_CostContact`, `Z_Revenue`)
2. **Exploratory Data Analysis**
    - Analyzed distributions (income, age, spending patterns)
    - Identified correlations (e.g., high correlation between meat purchases and catalog orders)
    - Visualized enrollment trends over time
3. **Clustering with K-Means**
    - Scaled data using `StandardScaler`
    - Applied PCA for dimensionality reduction (23 principal components)
    - Used the elbow method and silhouette scores to determine optimal clusters (k=2)
    - Profiled clusters using boxplots and barplots

### Key Insights

#### Cluster 0: *High-Engagement Customers*

- **Higher income** (mean: \$71,481) and **greater spending** across all categories
- **Responsive to campaigns** (higher acceptance rates)
- Fewer children/teens at home
- **Actionable strategy**: Target with premium offers and loyalty programs


#### Cluster 1: *Budget-Conscious Families*

- **Lower income** (mean: \$39,243) but **more website visits**
- More children/teens at home
- Higher complaint rates
- **Actionable strategy**: Focus on discounts, family bundles, and improved customer service


#### Overall Findings

- **Wine and meat** are top-selling categories
- **Catalog purchases** strongly correlate with higher-income segments
- Campaign 2 had the lowest acceptance rate (re-evaluate strategy)


### Repository Structure

- `Customer_Personality_Segmentation.csv`: Raw dataset
- `Tim_Roman_Full_Code_Version_Project_1.html`: Full analysis (preprocessing, EDA, modeling)
- `README.md`: Project overview (this file)


### How to Use

1. Review the HTML file for complete code and visualizations
2. Clone the repository to replicate analysis:
```bash

```

3. Key libraries: `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`

---
**Note**: This project demonstrates how data-driven segmentation enables personalized marketing and operational optimization. 


