# 👉 Superstore Sales & Profitability Analysis (End-to-End)
### Bridging Statistical Computing (R) and Business Intelligence (Power BI)

## 📌 Project Overview
This project transforms raw retail data into actionable business insights. By integrating **R** for data cleaning and **Power BI** for interactive visualization, I analyzed the Global Superstore dataset to understand the relationship between sales, discounts, and net profitability.

## 🛠️ Phase 1: Data Cleaning & Wrangling (R)
Using my background in computing, I ensured the data was pristine and structured for analysis.
- **Tools:** R (Tidyverse, Janitor).
- **Tasks:** Standardizing column names, handling missing values, and formatting date sequences.

```R
library(tidyverse)
library(janitor)

# Cleaning process
> df <- read_csv("Sample Superstore.csv")

> df_final <- df %>%
+ clean names() %>%
+ mutate(order_date = as.Date(order_date, format = "%m/%d/%Y"), sales = as.numeri
c(sales), profit = as.numeric(profit), discount = as.numeric(discount)) %>%
+ drop_na(sales, profit)

> print(paste("Number of rows:", nrow(df_final)))

> head(df_final)

# Exporting for Power BI
write_excel_csv(df_final, "Superstore_Final_Clean.csv")



 📊 Phase 2: Interactive Visual Analytics (Power BI)
​I built a dynamic dashboard to explore the data across three dimensions: Time, Geography, and Product Category.
​🔍 Key Insights:
​The Sales Spike: Identified a massive historical peak on March 14, 2014, driven by Corporate B2B bulk orders.
​Geospatial Clusters: Mapped sales density, revealing high market concentration in coastal metropolitan hubs.
​Discount vs. Profit: Used a Scatter Plot to prove that discounts exceeding 20% lead to significant profit erosion, especially in the Furniture category.
​💡 Business Recommendations
​Dynamic Pricing: Cap discounts at 15% for Furniture to protect margins.
​Inventory Focus: Prioritize Technology inventory as it yields the highest ROI.
​Expansion: Focus regional marketing on identified high-density clusters in the East Region.

### Dashboard Preview

![Main Dashboard](https://github.com/user-attachments/assets/84b9aa0c-079f-459d-aca2-afbf84b0dba2)

*Figure 1: Overall performance showing the sales spike in March 2014 and regional distribution.*

### Correlation Analysis

![Scatter Plot](https://github.com/user-attachments/assets/69d641b9-a327-459b-afb3-6ffb93da9afe)

*Figure 2: Scatter plot demonstrating the negative impact of high discounts on profit.*



## 🔍 Deep Dive & Analysis Insights

### 🛠️ Data Challenges & Solutions
> **Note:** As a junior data analyst, I am continuously learning. Below is a reflection on the technical hurdles I faced during this project.

During the initial visualization phase in **Power BI**, I encountered an issue where charts were not displaying correctly. I identified two main causes:
1. **Data Type Mismatch:** Some numerical columns were being treated as text.
2. **Hidden Whitespaces:** Leading/trailing spaces in the data were causing inconsistencies.

**The Solution:** By leveraging **R** for advanced data cleaning and utilizing AI-assisted debugging, I standardized the column types and removed inconsistencies. This ensured that the Power BI model could perform accurate calculations and render the visualizations correctly.

---

### 📈 Time-Series Analysis (Line Chart)
The sales trend reveals a significant **spike at the end of the Q1**. 
* **Hypothesis:** This suggests a highly successful launch marketing campaign or a large bulk order from a major client, indicating a very strong start for the company.
* **Seasonal Patterns:** We observe fluctuating patterns throughout the months, with a consistent **surge towards the end of the year**.
* **Business Impact:** This peak is likely due to holiday sales and year-end discounts. Understanding this seasonality allows the company to **forecast future sales** and optimize **inventory management** accordingly.

![Sales Trend Chart](https://github.com/user-attachments/assets/2acf21d3-bf92-4427-88ba-417c6bb0eecf)

---

### 🌍 Geospatial Analysis (Map Visualization)
The map highlights dense clusters of sales, revealing a strategic focus on **major urban hubs**. Key concentrations are visible in:
1. **The East Coast Cluster**
2. **California Region**
3. **The Great Lakes Region**

**Key Strategic Drivers:**
* **Supply Chain Efficiency:** The proximity of these cities facilitates easier shipping and reduces logistics costs. Sales naturally thrive in areas with high accessibility.
* **Demographic Correlation:** "Sales follow people." The high population density in these interconnected metropolitan areas directly correlates with the volume of transactions.

![Geospatial Map](https://github.com/user-attachments/assets/9e0bc8ab-92a4-41cb-aec6-de3f8e3d9f1b)



---

## 👤 Contact & Connect
**Project Created by:** [Mohammed El mojtaba]

- **LinkedIn:** [https://linkedin.com/in/mohamedelmojtaba]
- **GitHub:** [https://github.com/M-elmojtaba-code]

*Feel free to connect with me for any inquiries or data collaborations!*

---

### 🏷️ Keywords & Topics
`#DataAnalysis` `#PowerBI` `#RStats` `#BusinessIntelligence` `#DataVisualization` `#JuniorDataAnalyst` `#SalesForecasting` `#DataCleaning`
