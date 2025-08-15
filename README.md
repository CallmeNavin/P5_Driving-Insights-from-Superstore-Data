# Driving-Insights-from-Superstore-Data

**VERSION 1**

**A. Project Overview**

This project analyzes Sales, Profit, and Profit Margin for a retail superstore dataset using Power BI.
The focus is on identifying profitability trends, customer segments, product performance, shipping efficiency, and discount strategies.
The output includes:
- A multi-page Power BI dashboard with actionable business insights.
- A set of recommendations for improving profitability and operational efficiency.

**B. Dataset Information**
- Source: Sample Superstore Dataset (cleaned & filtered) 

https://www.kaggle.com/datasets/vivek468/superstore-dataset-final/data 
- Period: Jan 2014 – Dec 2017

**C. Methodology**

Data Cleaning & Preparation in Power Query:
- Removed outliers (Profit < 1000 dropped for margin clarity)
- Created calculated column for Profit Margin
- Grouped & aggregated data for key dimensions.

Exploratory Data Analysis (EDA):
- Trend analysis
- Top performance ranking
- Correlation between Discount & Profit Margin

Visualization in Power BI:
- KPI cards, line charts, bar charts, donut charts
- Segmentation by Category, Customer Segment, City, Product

**D. Dashboard Structure & Key Insights**

_**I. Sales & Profitability Overview**_

Key Findings:
- Q4 is peak season for profit.
- Technology has the highest profit margin → prioritize investment & expansion.
- Furniture has the lowest margin → optimize costs & supplier selection.

Actionable Insights:
- Focus marketing & inventory on Technology during Q4.
- Audit Furniture supply chain to improve margin.

_**II. Profit Margin Trends**_

Key Findings:
- Office Supplies maintains stable & high margins.
- Technology shows volatility but good margins overall.
- Consumer Segment yields higher margins vs Corporate & Home Office.

Actionable Insights:
- Stabilize Technology margin through supply & pricing strategy.
- Target campaigns at Consumer Segment.

_**III. Customer Profile**_

Key Findings:
- 51% of customers are Consumers, but Home Office yields the highest margin.
- Philadelphia city stands out with negative profit.

Actionable Insights:
- Strengthen loyalty programs for top-spending customers.
- Investigate Philadelphia’s losses → adjust pricing & operations.

_**IV. Product Analysis**_

Key Findings:
- Office Supplies has the most SKUs.
- Highest margin products: Labels, Paper, Envelopes (all Office Supplies).
- Some high-volume products have low margin (Binder, Art).

Actionable Insights:
- Focus marketing & production on Office Supplies for Home Office segment.
- Negotiate with suppliers or adjust pricing for low-margin, high-volume products.

_**V. Order & Shipping**_

Key Findings:
- Standard Class accounts for >50% of orders.
- 40% of orders have shipping delay (>5 days).

Actionable Insights:
- Reduce delivery time for Standard Class.
- Consider shifting part of orders to faster shipping methods.

_**VI. Discount Strategy**_

Key Findings:
- High discounts can boost sales but reduce margins depending on category.
- Central region applies the most discounts.
- Furniture has low margin yet high discounts.

Actionable Insights:
- Optimize discount levels based on margin threshold.
- Limit discounts for Furniture while improving quality & service.

**E. Next Steps**
- Extend analysis to predictive modeling (Sales & Profit Forecasting)
- Develop price elasticity model for discount optimization

**VERSION 2**

**F. Methods**

I applied Linear Regression and Random Forest Regressor models to predict Profit. 
Among them, the Random Forest Regressor demonstrated higher accuracy and reliability.

**G. Dashboard Structure & Key Insights**

_**VII. Predictive Analysis**_

Key Findings:

- Random Forest outperforms Linear Regression significantly:
  MAE reduced from 50.0 to 20.3 (~60% improvement).
  RMSE reduced from 111.6 to 68.4 (~39% improvement).
  R² increased from 0.6166 to 0.8558, meaning the model explains 85.6% of the variation in Profit.
- The top three factors impacting Profit the most are Sales, Discount, and Quantity

Actionable Insights:

- Adopt Random Forest for future profit prediction tasks.
- Optimize pricing and discount strategies, as they have the strongest effect on profitability.
- Adjust inventory planning and sales campaigns based on Quantity sold to improve profit margins.

**VERSION 3 - TUNING**

Attempted hyperparameter tuning using RandomizedSearchCV. The tuned model did not outperform the baseline Random Forest, so the original model was retained for final use.

**H. About Me**

Hi, I'm Navin – an aspiring Data Analyst passionate about turning raw data into actionable business insights.

Follow me at: 
- 🌐 LinkedIn: https://www.linkedin.com/in/navin826/
- 📂 Portfolio: https://github.com/CallmeNavin/

_**Notes:**_

This dashboard.pbix contains both Descriptive (v1) and Predictive (v2) analysis. Updated regularly based on the latest data.
