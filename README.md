# CustomerBehaviourAnalysis
This project explores customer shopping behaviour using Python, SQL, Excel, PowerBI

---

# **Customer Shopping Behavior Analysis**

## **1. Project Overview**

This project explores **customer shopping behavior** using transactional data from **3,900 purchases** across multiple product categories. The objective is to uncover insights related to **spending patterns, customer segments, product preferences, and subscription behavior**, enabling data-driven strategic decisions for improved customer engagement and revenue growth.

---

## **2. Dataset Summary**

* **Total Rows:** 3,900
* **Columns:** 18
* **Key Features Include:**

  * **Customer Demographics:** Age, Gender, Location, Subscription Status
  * **Purchase Details:** Item Purchased, Category, Purchase Amount, Season, Size, Color
  * **Behavioral Indicators:** Discount Applied, Previous Purchases, Purchase Frequency, Review Ratings, Shipping Type
* **Missing Data:**

  * 37 missing entries in the *Review Rating* column, handled via imputation

---

## **3. Exploratory Data Analysis (Python)**

The EDA phase focused on cleaning, transforming, and preparing the data for deeper analysis:

### **Data Preparation**

* Loaded the dataset using **pandas**.
* Performed structural checks with `.info()` and statistical summaries using `.describe()`.

### **Data Cleaning**

* Identified and imputed missing values in *Review Rating* using the **median rating per product category**.
* Standardized column names to **snake_case** for better readability and consistency.

### **Feature Engineering**

* Created an **age_group** feature by binning age ranges.
* Generated a **purchase_frequency_days** metric from timestamps.
* Assessed redundancy between *discount_applied* and *promo_code_used* — removed *promo_code_used* to avoid duplication.

### **Database Integration**

* Connected the cleaned dataset to **PostgreSQL**.
* Loaded the transformed DataFrame into the database for SQL-based business analysis.

---

## **4. SQL-Based Business Analysis**

Using PostgreSQL, we answered several key business questions:

1. **Revenue by Gender** – Compared total spending between male and female customers.
2. **High-Spending Discount Users** – Identified customers who applied discounts but still spent above the overall average.
3. **Top 5 Products by Review Rating** – Ranked products based on their average customer ratings.
4. **Shipping Type Analysis** – Compared average purchase amounts for Standard vs. Express shipping.
5. **Subscriber vs. Non-Subscriber Behavior** – Analyzed spend levels and revenue contribution by subscription status.
6. **Discount-Dependent Products** – Identified products with the highest proportion of discounted purchases.
7. **Customer Segmentation** – Categorized customers as **New**, **Returning**, or **Loyal** based on purchase frequency.
8. **Top Products per Category** – Extracted the top 3 most purchased products within each category.
9. **Repeat Buyers & Subscription Likelihood** – Examined whether customers with more than 5 purchases are more likely to be subscribers.
10. **Revenue by Age Group** – Measured revenue contribution across age segments.

---

## **5. Power BI Dashboard**

An interactive dashboard was built using **Power BI**, featuring:

* Revenue insights
* Customer segmentation visuals
* Product performance metrics
* Discount utilization patterns
* Age, gender, and geographic breakdowns

The dashboard provides a clear visual narrative of customer behavior and purchasing trends.

---

## **6. Business Recommendations**

Based on our analysis, we propose the following strategies:

* **Boost Subscriptions:** Highlight exclusive benefits and run targeted subscription campaigns.
* **Strengthen Loyalty Programs:** Reward returning customers to convert them into loyal, high-value customers.
* **Optimize Discount Strategy:** Offer discounts strategically to boost conversions without eroding margins.
* **Enhance Product Positioning:** Promote top-rated and best-selling products to increase conversions.
* **Targeted Marketing Efforts:** Prioritize high-revenue age groups and express-shipping customers for targeted outreach.

---
