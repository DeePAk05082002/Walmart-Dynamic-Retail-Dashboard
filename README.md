# Dynamic Retail Dashboard
---
## Overview

The **Dynamic Retail Dashboard** is a comprehensive and interactive Excel-based tool designed to provide insights into retail operations. It leverages advanced Excel features such as Power Query for data transformation and dynamic visualizations to deliver actionable insights for decision-making. The dashboard connects seamlessly to GitHub-hosted data sources, making it scalable and adaptable for real-world use cases.
---
###Significance
Retail operations involve diverse data sources and complex relationships between orders, returns, and customer behavior. The Dynamic Retail Dashboard simplifies these complexities by:

- Consolidating multiple datasets into a unified interface.
- Providing insights into sales performance, profitability, and customer behavior.
- Supporting decision-making with real-time dynamic visualizations.
- Enhancing the ability to track and optimize key metrics such as sales trends, profit margins, and category performance.
---

### Key Features:

- Integration with GitHub-hosted data tables.
- Powerful data transformation using Power Query.
- Interactive KPIs and dynamic charts.
- In-depth analysis of sales, profit, and customer behavior.
- Customizable and scalable for future enhancements.

---

## Data Dictionary

### Orders Table:

| Column Name    | Description                                                |
| -------------- | ---------------------------------------------------------- |
| Order ID       | Unique identifier for each order.                          |
| Order Date     | Date when the order was placed.                            |
| Ship Date      | Date when the order was shipped.                           |
| Ship Mode      | Shipping mode (e.g., Same Day, Second Class).              |
| Customer ID    | Unique identifier for the customer.                        |
| Customer Name  | Name of the customer.                                      |
| Segment        | Customer segment (e.g., Consumer, Corporate, Home Office). |
| City           | City where the order was placed.                           |
| State          | State where the order was placed.                          |
| Country        | Country where the order was placed.                        |
| Postal Code    | Postal code of the order location.                         |
| Market         | Market region of the order (e.g., US, EU, APAC).           |
| Region         | Geographic region of the order.                            |
| Product ID     | Unique identifier for the product.                         |
| Category       | Product category (e.g., Technology, Furniture).            |
| Sub-Category   | Product sub-category.                                      |
| Product Name   | Name of the product.                                       |
| Sales          | Total sales amount for the order.                          |
| Quantity       | Quantity of items in the order.                            |
| Discount       | Discount applied to the order.                             |
| Profit         | Profit earned from the order.                              |
| Shipping Cost  | Shipping cost for the order.                               |
| Order Priority | Priority of the order (e.g., Critical, High, Medium).      |

**Sample Data:**

| Order ID       | Order Date | Ship Date  | Ship Mode    | Customer ID | Customer Name | Segment   | City          | State      | Country       | Postal Code | Market | Region  | Product ID      | Category   | Sub-Category | Product Name                                                | Sales   | Quantity | Discount | Profit  | Shipping Cost | Order Priority |
| -------------- | ---------- | ---------- | ------------ | ----------- | ------------- | --------- | ------------- | ---------- | ------------- | ----------- | ------ | ------- | --------------- | ---------- | ------------ | ----------------------------------------------------------- | ------- | -------- | -------- | ------- | ------------- | -------------- |
| CA-2012-124891 | 31-7-2020  | 31-7-2020  | Same Day     | RH-19495    | Rick Hansen   | Consumer  | New York City | New York   | United States | 10024       | US     | East    | TEC-AC-10003033 | Technology | Accessories  | Plantronics CS510 - Over-the-Head monaural Wireless Headset | 2309.65 | 7        | 0        | 762.18  | 933.57        | Critical       |
| IN-2013-77878  | 5-2-2021   | 7-2-2021   | Second Class | JR-16210    | Justin Ritter | Corporate | Wollongong    | New South  | Australia     |             | APAC   | Oceania | FUR-CH-10003950 | Furniture  | Chairs       | Novimex Executive Leather Armchair, Black                   | 3709.39 | 9        | 0.1      | -288.76 | 923.63        | Critical       |
| IN-2013-71249  | 17-10-2021 | 18-10-2021 | First Class  | CR-12730    | Craig Reiter  | Consumer  | Brisbane      | Queensland | Australia     |             | APAC   | Oceania | TEC-PH-10004664 | Technology | Phones       | Nokia Smart Phone, with Caller ID                           | 5175.17 | 9        | 0.1      | 919.97  | 915.49        | Medium         |

### Returns Table:

| Column Name | Description                                        |
| ----------- | -------------------------------------------------- |
| Returned    | Indicates whether the order was returned (Yes/No). |
| Order ID    | Identifier for the returned order.                 |
| Market      | Market region of the returned order.               |

**Sample Data:**

| Returned | Order ID        | Market        |
| -------- | --------------- | ------------- |
| Yes      | MX-2013-168137  | LATAM         |
| Yes      | US-2011-165316  | LATAM         |
| Yes      | ES-2013-1525878 | EU            |
| Yes      | CA-2013-118311  | United States |
| Yes      | IN-2014-58460   | APAC          |

### People Table:

| Column Name | Description                                       |
| ----------- | ------------------------------------------------- |
| Person      | Name of the individual.                           |
| Region      | Geographic region associated with the individual. |

**Sample Data:**

| Person            | Region  |
| ----------------- | ------- |
| Anna Andreadi     | Central |
| Chuck Magee       | South   |
| Kelly Williams    | East    |
| Matt Collister    | West    |
| Deborah Brumfield | Africa  |

---

## Steps to Create the Dashboard

### 1. Data Integration

- Host the `Orders`, `People`, and `Returns` tables on your GitHub repository.
- Use Excel’s **Get Data** feature to connect to GitHub and import the tables into the workbook.

### 2. Data Transformation in Power Query

- Load all the tables into Power Query.
- Perform the following transformations:
  - **Orders Table**: Clean and shape the data, removing unnecessary columns and ensuring proper data types.
  - **Returns Table**: Merge with the Orders table to create a unified dataset.
  - **People Table**: Join with the Orders table for region-based analysis.

### 3. KPI Creation

- Create a dedicated KPI table with the following metrics:
  | KPI Name       | Description                      | Symbol |
  | -------------- | -------------------------------- | ------ |
  | Total Sales    | Sum of sales across all orders.  | 💰     |
  | Total Profit   | Sum of profit across all orders. | 📈     |
  | Total Quantity | Sum of quantities ordered.       | 📦     |
  | Total Orders   | Count of unique order IDs.       | 🛒     |
  | Profitability  | Ratio of profit to sales.        | 💹     |

### 4. Build Visualizations

- Use Excel’s charting tools to create the following visualizations:
  - **Sales and Profit Analysis**: Compare sales and profit trends.
  - **Category-Wise Profit**: Visualize profit distribution across product categories.
  - **Segment-Wise Sales Share**: Highlight the percentage contribution of each segment to total sales.
  - **Sales by Country**: Map sales distribution across countries.
  - **Yearly Sales Trend**: Analyze trends over time using line charts.
  - **Top and Bottom Sub-Categories**: Identify top-performing and least-performing sub-categories.

### 5. Dashboard Design

- Arrange the visuals and KPIs in a clean, intuitive layout.
- Add slicers to filter data dynamically by:
  - Region
  - Category
  - Year
- Ensure the dashboard is aesthetically pleasing and easy to navigate.

---

## Problem Statements Solved

### 1. **Key Performance Indicators (KPIs):**

- **Objective:** Summarize critical metrics for quick insights.
- **Approach:** Calculate metrics such as Total Sales, Profit, Quantity, Number of Orders, and Profit Margin using Excel formulas and Power Query.
- **Visual Required:** Card-style KPI visualizations.
- **Hint:** Use `SUM`, `COUNT`, and custom measures in Power Query or PivotTables for calculations.
  
  ![image](https://github.com/user-attachments/assets/5293c346-3f80-4dd4-b6da-b692b2b7fb70)

---
### 2. **Sales and Profit Analysis**:

- **Objective:** Compare sales and profit across regions, categories, and time.
- **Approach:** Create a PivotTable or PivotChart to analyze trends.
- **Visual Required:** Line or bar charts.
- **Hint:** Use slicers to drill down into specific time periods or regions.
  
  ![image](https://github.com/user-attachments/assets/ca4cea6d-5a51-4569-9c7c-944a597897bb)

---
### 3. **Category-Wise Profit Analysis**:

- **Objective:** Identify profitable and non-profitable categories.
- **Approach:** Group data by categories and calculate total profit per category.
- **Visual Required:** Column or pie charts.
- **Hint:** Sort categories by profit to highlight trends.
  
  ![image](https://github.com/user-attachments/assets/f29a36c4-6bb0-4daf-b3e0-5f1945c94439)

---
### 4. **Segment-Wise Sales Share**:

- **Objective:** Visualize sales contributions from different customer segments.
- **Approach:** Calculate the percentage contribution of each segment to total sales.
- **Visual Required:** Pie or donut charts.
- **Hint:** Use `SUMIF` or PivotTables for segment-specific calculations.
  
  ![image](https://github.com/user-attachments/assets/959d3f5e-01ee-4f32-9fa2-d8cbeb8845d7)

---
### 5. **Sales by Country**:

- **Objective:** Highlight top-performing countries in terms of sales.
- **Approach:** Group data by country and aggregate sales.
- **Visual Required:** Map charts or column charts.
- **Hint:** Utilize Power Query for grouping and aggregation.
  
  ![image](https://github.com/user-attachments/assets/c6bfd637-1ec3-4daf-8c12-c8422740a8f2)

---
### 6. **Top 5 Sub-Categories**:

- **Objective:** Determine the most successful sub-categories by sales and profit.
- **Approach:** Sort data by sales or profit and select the top 5 entries.
- **Visual Required:** Bar or column charts.
- **Hint:** Use filters or rankings in PivotTables.
  
  ![image](https://github.com/user-attachments/assets/803fc37f-204a-4213-9df4-0eb25edc3528)

---
### 7. **Bottom 5 Sub-Categories**:

- **Objective:** Identify the least performing sub-categories.
- **Approach:** Sort data in ascending order by sales or profit and select the bottom 5 entries.
- **Visual Required:** Bar or column charts.
- **Hint:** Highlight negative trends using conditional formatting.
  
   ![image](https://github.com/user-attachments/assets/d0dad0f6-4f06-46db-8e32-e42068298656)

---
### 8. Yearly Sales Trends
- Objective: Visualize sales trends over the years to spot growth or decline patterns.
- Approach: Aggregate sales data by year and plot it using a line chart.
- Visual: Line chart with markers for yearly sales values.
- Hint: Overlay profit trends on the same chart for a dual-axis comparison of sales and profitability.
  
  ![image](https://github.com/user-attachments/assets/d6a89241-9d92-4d5d-bdb8-14a4dbf189d0)


---
### Future Scope
- Return Analysis: Explore patterns in returned orders by region, category, or segment.
- Customer Analysis: Identify top and bottom customers based on profitability.
- Market Trends: Analyze market-wise performance over time.
- 
---
### Visuals
This repository includes:
- Visual examples for each solved problem statement.
- Snapshots of the final dashboard with all components.
![image](https://github.com/user-attachments/assets/a3cc167d-1332-4580-b653-8326d8901f0d)




