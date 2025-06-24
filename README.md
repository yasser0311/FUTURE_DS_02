````markdown
# 📊 Marketing Campaign Analytics Dashboard - Power BI

This Power BI dashboard project provides a comprehensive analysis of customer demographics, campaign effectiveness, and product purchase behaviors based on a cleaned marketing dataset.

---

## 📁 Dataset Source

**File:** `cleaned_marketing_data.csv`  
**Structure:** Cleaned version of the original marketing dataset, with transformed fields:
- Cleaned `Income` column
- Converted `Dt_Customer` to date format
- Added derived fields: `TotalChildren`, `TotalSpent`, `TotalAcceptedCmp`, `Age`

---

## 🎯 Project Objectives

- Analyze customer segments by age, education, and marital status
- Understand purchasing behavior across different product categories
- Evaluate marketing campaign effectiveness (5 campaigns + final response)
- Create actionable insights using DAX measures and interactive visuals

---

## 🧠 DAX Measures Created

```DAX
Total Campaign Responses = SUM(cleaned_marketing_data[TotalAcceptedCmp])

Response Rate (%) = 
DIVIDE(SUM(cleaned_marketing_data[Response]), COUNT(cleaned_marketing_data[ID]), 0)

Estimated Revenue = 
SUM(cleaned_marketing_data[TotalAcceptedCmp]) * 1000

Average Income = AVERAGE(cleaned_marketing_data[Income])

Average Spending = AVERAGE(cleaned_marketing_data[TotalSpent])

Average Total Children = AVERAGE(cleaned_marketing_data[TotalChildren])
````

---

## 🖥️ Power BI Dashboard Layout

### 📌 Page 1: Customer Overview

* Cards: Total Customers, Average Age, Income, Recency
* Bar Chart: Age Distribution
* Donut Charts: Education and Marital Status
* Timeline: Customer Joining Trend

### 📌 Page 2: Campaign Effectiveness

* KPI Cards: Total Campaign Responses, Response Rate
* Stacked Bar: AcceptedCmp1–5 distribution
* Pie Chart: Response by Country
* Bar: Education vs TotalAcceptedCmp

### 📌 Page 3: Purchase Behavior

* Bar Charts: Spending by Product Categories
* Channel Preferences: Web, Catalog, Store Purchases
* Slicers: Age, Country, Education, Marital Status

---

## 📌 How to Use

1. Open Power BI Desktop
2. Load `cleaned_marketing_data.csv`
3. Rename table to `cleaned_marketing_data` (if needed)
4. Create the above DAX measures under *Modeling > New Measure*
5. Build visuals as per the layout described above
6. Style with slicers, labels, and formatting for readability

---

## 💡 Insights You Can Extract

* Which customer group spends the most?
* Which campaign had the best acceptance rate?
* How does education level impact campaign response?
* What products are most purchased across age groups?

---

## 🛠️ Tools Used

* Power BI Desktop
* DAX for calculated metrics
* Pandas (Python) for data cleaning and transformation

---

## 👨‍💻 Author

**Mohammed Yasser**
Aspiring Data Scientist | Marketing Analytics Enthusiast
🔗 [LinkedIn Profile](https://www.linkedin.com/in/yasser-reyvan)

---

## 📬 Feedback / Questions

Feel free to raise an issue or contact me on LinkedIn for suggestions, contributions, or questions!

```
