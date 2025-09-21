# Driving-Insights-from-Superstore-Data

**VERSION 1 - DESCRIPTIVE ANALYSIS**

**A. Project Overview**

This project analyzes Sales, Profit, and Profit Margin for a retail superstore dataset using Power BI.
The focus is on identifying profitability trends, customer segments, product performance, shipping efficiency, and discount strategies.
The output includes:
- A multi-page Power BI dashboard with actionable business insights.
- A set of recommendations for improving profitability and operational efficiency.

![Dashboard Visualization](https://github.com/CallmeNavin/P5_Driving-Insights-from-Superstore-Data/blob/main/Version%201%20-%20Descriptive%20Analytics/Visualization/Dashboard.png)

_Explore more insights in the full Power BI dashboard_

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

**D. Key Findings & Actionable Plans**

_**I. Sales & Profitability Overview**_

Key Findings:
- Q4 is peak season for profit.
- Technology has the highest profit margin → prioritize investment & expansion.
- Furniture has the lowest margin → optimize costs & supplier selection.

Actionable Plans:
- Focus marketing & inventory on Technology during Q4.
- Audit Furniture supply chain to improve margin.

_**II. Profit Margin Trends**_

Key Findings:
- Office Supplies maintains stable & high margins.
- Technology shows volatility but good margins overall.
- Consumer Segment yields higher margins vs Corporate & Home Office.

Actionable Plans:
- Stabilize Technology margin through supply & pricing strategy.
- Target campaigns at Consumer Segment.

_**III. Customer Profile**_

Key Findings:
- 51% of customers are Consumers, but Home Office yields the highest margin.
- Philadelphia city stands out with negative profit.

Actionable Plans:
- Strengthen loyalty programs for top-spending customers.
- Investigate Philadelphia’s losses → adjust pricing & operations.

_**IV. Product Analysis**_

Key Findings:
- Office Supplies has the most SKUs.
- Highest margin products: Labels, Paper, Envelopes (all Office Supplies).
- Some high-volume products have low margin (Binder, Art).

Actionable Plans:
- Focus marketing & production on Office Supplies for Home Office segment.
- Negotiate with suppliers or adjust pricing for low-margin, high-volume products.

_**V. Order & Shipping**_

Key Findings:
- Standard Class accounts for >50% of orders.
- 40% of orders have shipping delay (>5 days).

Actionable Plans:
- Reduce delivery time for Standard Class.
- Consider shifting part of orders to faster shipping methods.

_**VI. Discount Strategy**_

Key Findings:
- High discounts can boost sales but reduce margins depending on category.
- Central region applies the most discounts.
- Furniture has low margin yet high discounts.

Actionable Plans:
- Optimize discount levels based on margin threshold.
- Limit discounts for Furniture while improving quality & service.

**VERSION 2 - PREDICTIVE ANALYSIS**

**A. Project Overview**

- Applied Linear Regression and Random Forest Regressor models to predict Profit. 

**B. Key Findings & Actionable Plans**

_**Key Findings**_

- Random Forest outperforms Linear Regression significantly:
  MAE reduced from 50.0 to 20.3 (~60% improvement).
  RMSE reduced from 111.6 to 68.4 (~39% improvement).
  R² increased from 0.6166 to 0.8558, meaning the model explains 85.6% of the variation in Profit.
- The top three factors impacting Profit the most are Sales, Discount, and Quantity

_**Actionable Plans**_

- Adopt Random Forest for future profit prediction tasks.
- Optimize pricing and discount strategies, as they have the strongest effect on profitability.
- Adjust inventory planning and sales campaigns based on Quantity sold to improve profit margins.

**VERSION 3 - TUNING**

Attempted hyperparameter tuning using RandomizedSearchCV. The tuned model did not outperform the baseline Random Forest, so the original model was retained for final use.

**VERSION 4 - TIME-SERIES FORECASTING**

**A. Project Overview**

- This project predict future profit based on Order Date using Time-series models, comparing simple baseline models to SARIMAX to identify the best approach.

**B. Methodology**

- Basic EDA
- Actions after Basic EDA:
  + Change dtype of 'Order Date', 'Ship Date' column from object to datetime
- Predictive Analysis Setup:
  + Set the time index to Order Date
  + Resample by Week
  + Group by Category
  + Train/Test Split
- Modeling:
  + Naive Forecast
  + Exponential Smoothing (Holt-Winters)
  + SARIMAX

**C. Key Findings & Actionable Plans**

_**Key Findings**_

![SARIMAX Result](https://github.com/CallmeNavin/P5_Driving-Insights-from-Superstore-Data/blob/main/Version%204%20-%20Time-Series%20Forecasting/Visualization/SARIMAX%20Result.png)

- Best model: SARIMA(1,1,1) × (1,1,0,52)
- Baseline AIC = 1894.6 while Best model AIC = 900.72 → SARIMAX Model after fix is better than Baseline Models (Naive Forecast, Exponential Smoothing (Holt-Winters))
- MAPE ~ 2% → Mostly Exact Prediction

**_Actionable Plans_**

- Leverage SARIMAX model as a profit monitoring tool: compare forecasted profit against actual results to evaluate business performance and improve forecasting accuracy over time:
  + Detect upcoming downturns in profit and proactively adjust strategies
  + Utilize the weekly profit forecasts to support financial planning and budget allocation.

**About Me**

Hi, I'm Navin – an aspiring Data Analyst passionate about turning raw data into actionable business insights.

Follow me at: 
- 🌐 LinkedIn: https://www.linkedin.com/in/navin826/
- 📂 Portfolio: https://github.com/CallmeNavin/
