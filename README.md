# 🛍️ Customer Shopping Behavior Analysis

## 1. Project Overview
This project transforms raw transactional data into a strategic **Power BI Dashboard** to identify growth opportunities. By analyzing **3.9K purchases**, I uncovered high-impact insights regarding gender-based pricing disparities, seasonal revenue trends, and geographical performance to guide executive decision-making.

---

## 🖼️ Interactive Dashboard View
![Final Dashboard Screenshot](images/your_screenshot_name.png)
> *Note: Download the .pbix file in this repo to explore the interactive filters.*

---

## 2. Dataset Summary (Dashboard Scope)
* **Scale:** 3,900 Rows | 18 Columns
* **Key Features Analyzed:**
    * **Demographics:** Age, Gender, Location (State).
    * **Transactions:** Category, Purchase Amount (USD), Season.
    * **Behavior:** Discount Applied, Review Rating, Previous Purchases.

---

## 3. Data Preparation & Engineering (Python)
I performed targeted cleaning to ensure the dashboard's accuracy and integrity:
* **Missing Data Handling:** Imputed missing values in `Review Rating` using the **median rating per category**.
* **Standardization:** Converted features to `snake_case` for seamless SQL/Power BI integration.
* **Feature Engineering:** * Created `age_group` bins (Young Adult, Middle-aged, Adult, Senior).
    * Classified `customer_segment` (New, Returning, Loyal) based on purchase history.
* **Database Integration:** Migrated cleaned data to **PostgreSQL** to serve as a structured "Single Source of Truth."

---

## 4. Strategic Analysis (SQL)
Before visualization, I performed structured queries in **PostgreSQL** to validate core business metrics:
* **Revenue by Gender:** Identified the primary revenue-contributing demographic.
* **Loyalty Metrics:** Analyzed retention strength across gender segments.
* **Pricing Analysis:** Isolated promotional frequency to check for discount dependency.
* **Geographical Ranking:** Identified "Market Leaders" and "Revenue Risks" by State.

---

## 5. Strategic Business Recommendations
Based on the dashboard discoveries, I proposed the following actions:
* **Fix the Loyalty Gap:** Males (25.8 Visits) lead in retention but are **63% Discount-Driven**. Females (24.6 Visits) are **Organic buyers (0% discount)**. I recommend a **10% 'Loyalty Reward'** for Females to scale this high-margin segment.
* **Optimize Seasonal Inventory:** Young Adults dominate **Winter Clothing** spend. Recommend prioritizing Q4 marketing spend on "Style-Focused" campaigns for this group.
* **Geographical Audit:** Investigate **Rhode Island** and **Kansas** (Bottom 5) for supply chain or competitive issues to replicate the success seen in **Montana**.
