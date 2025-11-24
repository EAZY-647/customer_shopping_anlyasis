
# Customer Shopping Behavior Analysis

## Overview
This portfolio project explores customer shopping behavior using transactional data from 3,900 purchases across multiple product categories. The objective is to uncover insights into spending patterns, customer segmentation, product preferences, and subscription dynamics to support strategic decision-making in retail.

---

## Business Context
Retail businesses often struggle to balance promotional strategies, customer retention, and product positioning. This analysis addresses key questions such as:
- Which customer segments generate the most revenue?
- How do discounts and subscriptions influence spending?
- What products perform best in terms of ratings and sales?
- How can loyalty and marketing efforts be optimized?

---

## Dataset Summary
- **Source:** Synthetic transactional data  
- **Size:** 3,900 rows × 18 columns  
- **Key Features:**
  - Customer demographics: Age, Gender, Location, Subscription Status  
  - Purchase details: Item, Category, Amount, Season, Size, Color  
  - Shopping behavior: Discounts, Frequency, Review Ratings, Shipping Type  
- **Missing Data:** 37 null values in the Review Rating column  
- **File:** `customer_shopping_behavior.csv`

---

## Methodology

### Data Preparation (Python)
- Imported dataset using Pandas and performed initial exploration (`df.info()`, `df.describe()`).
- Imputed missing review ratings using median values per product category.
- Standardized column names to snake_case for consistency.
- Engineered features:
  - `age_group` (binned age ranges)
  - `purchase_frequency_days` (derived from transaction history)
- Removed redundant `promo_code_used` column.
- Loaded cleaned data into PostgreSQL for structured querying.

### Business Analysis (SQL)
Executed targeted queries to answer key business questions:
- Revenue by gender and age group
- High-spending discount users
- Top-rated products
- Shipping type comparison
- Subscriber vs. non-subscriber behavior
- Discount-dependent products
- Customer segmentation (New, Returning, Loyal)
- Repeat buyers and subscription correlation
- Top products per category

### Visualization (Power BI)
Built an interactive dashboard to present insights:
- Revenue and sales by category, age group, and subscription status
- Customer loyalty distribution
- Shipping type impact on spending
- Key metrics:
  - Average Purchase Amount: $59.76
  - Average Review Rating: 3.75
  - Subscription Rate: 27% Yes, 73% No

---

## Key Insights
- Male customers generated nearly twice the revenue of female customers.
- Young Adults contributed the highest revenue among age groups.
- Loyal customers formed the majority segment (80%+).
- Express shipping correlated with higher spending.
- Discount-heavy products (e.g., Hats, Sneakers) may require margin review.
- Repeat buyers were more likely to subscribe.

---

## Recommendations
1. Promote exclusive benefits to increase subscriptions.
2. Incentivize repeat buyers to transition into loyal customers.
3. Balance discount strategy to protect margins.
4. Highlight top-rated and best-selling products in campaigns.
5. Focus marketing on high-revenue age groups and express shipping users.

---

## Tools & Technologies
- **Python (Pandas, NumPy):** Data cleaning and feature engineering  
- **PostgreSQL:** Structured business queries  
- **Power BI:** Interactive dashboard development  
- **Excel:** Supporting analysis and validation  

---

## Project Files

| File Name                                | Description                                                                 |
|------------------------------------------|-----------------------------------------------------------------------------|
| `customer_shopping_behavior.csv`         | Raw transactional dataset                                                   |
| `Customer_Shopping_Behavior_Analysis.ipynb` | Python notebook for data preparation and PostgreSQL integration             |
| `customer_behavior_sql_queries.sql`      | SQL scripts for business analysis                                           |
| `customer_behavior_dashboard.pbix`       | Power BI dashboard file                                                     |
| `customer_shopping.pdf`                  | Original project report                                                     |
| `Business Problem_Document.pdf`          | Business context and problem framing document                               |

---

## How to Reproduce

1. **Clone the repository** and place all files in the working directory.  
2. **Run the Jupyter notebook** (`Customer_Shopping_Behavior_Analysis.ipynb`) to clean and transform the data.  
3. **Set up PostgreSQL** and import the cleaned dataset using the notebook’s database integration steps.  
4. **Execute SQL queries** from `customer_behavior_sql_queries.sql` to generate insights.  
5. **Open the Power BI dashboard** (`customer_behavior_dashboard.pbix`) to explore visualizations interactively.

---

## Portfolio Value
This project demonstrates:
- End-to-end analytics capability from raw data to business recommendations
- Integration of Python, SQL, and BI tools for scalable analysis
- Strategic thinking and stakeholder-ready presentation
- Reproducible workflows and clean documentation for professional audiences

---

