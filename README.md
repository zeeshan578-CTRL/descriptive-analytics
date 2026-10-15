#  

🛒 Zepto Quick Commerce Data Analysis

A Deep Dive into Delivery Performance, Customer Ordering Behaviour, Product Demand, Dark-Store Operations & Inventory Risk

A comprehensive Descriptive Analytics project exploring how data can help a quick-commerce business understand its operational performance, identify demand patterns, monitor delivery SLA risks, optimize inventory management, and make better business decisions.

---

📌 Project Overview

Quick commerce has transformed the way customers purchase everyday essentials by promising fast deliveries, convenient ordering, and the availability of products whenever customers need them. However, delivering orders within a short time frame requires much more than a well-designed application. It depends on effective inventory management, accurate demand planning, efficient dark-store operations, rider availability, and continuous monitoring of operational performance.

This project, Zepto Quick Commerce Data Analysis, explores these challenges through a structured descriptive analytics workflow. It focuses on understanding what happened during a defined observation period, identifying meaningful patterns in the data, and translating analytical findings into practical business recommendations.

The project investigates product-level order performance, delivery-time distribution, Service Level Agreement (SLA) breaches, peak ordering windows, weekday-versus-weekend demand, regional order concentration, and product-level inventory risks.

Rather than treating data analysis as a process of simply calculating totals and generating charts, this project approaches analytics from a business perspective: every metric should help answer a question, every visualization should reveal a useful pattern, and every finding should support a potential operational decision.

The analysis is structured around five major business questions:

1. Which products generate the highest order volumes, and how concentrated is demand among the best-selling products?
2. How does delivery performance change over time, and which dark-store zone shows the strongest signs of SLA risk?
3. When do customers place the most orders, and how do ordering patterns differ between weekdays and weekends?
4. Which dark-store zones contribute the greatest share of total demand, and what does this mean for fulfillment planning?
5. Which products are approaching inventory depletion, and how can stockout risks be identified before they affect customers?

By answering these questions, the project demonstrates how descriptive analytics can turn structured operational data into insights that are relevant to category management, inventory planning, delivery operations, and business performance monitoring.

«Important data note: This project uses a synthetic dataset created for educational and analytical practice. It is not based on live Zepto transactions or confidential company records. The findings describe the constructed dataset and should not be interpreted as verified statements about Zepto's actual business performance.»

---

🎯 Project Objectives

The primary objective is to build a descriptive analytics layer that summarizes quick-commerce activity and identifies patterns that could matter to business operations.

The specific objectives are:

- Product Performance Analysis: Identify best-selling products, rank SKUs by order volume, calculate leading-product contribution, and understand the concentration of demand across the product portfolio.
- Delivery Performance Monitoring: Examine average delivery times, compare performance against a 10-minute SLA target, and identify zones where delivery times show an upward trend.
- Customer Ordering Pattern Analysis: Investigate demand across time-of-day bands and days of the week to identify peak ordering periods and recurring demand differences.
- Regional Demand Analysis: Compare order volumes across dark-store zones, identify high-demand locations, and understand the operational implications of uneven demand distribution.
- Inventory Risk Analysis: Classify product stock status, estimate days of supply, identify products requiring replenishment attention, and explain how reorder-point logic can support inventory decisions.
- Business Recommendation Development: Convert numerical results into practical recommendations for staffing, rider allocation, shelf placement, replenishment, and operational monitoring.
- Future Analytics Planning: Identify how the descriptive reporting layer could be extended into predictive analytics through demand forecasting, delivery-time forecasting, and anomaly detection.

---

📊 Dataset Description

The project uses a synthetic quick-commerce dataset designed to resemble an aggregated operational reporting table.

Dataset Specifications

Attribute| Description
Business domain| Quick commerce and online grocery delivery
Dataset type| Synthetic, educational dataset
Observation period| July 1–15, 2026
Number of products| 10
Number of dark-store zones| 5
Number of product-day records| 150
Analysis approach| Descriptive analytics
Primary analytical unit| Product-day record associated with a dominant dark-store zone

Each row represents the aggregated daily activity of a product in its dominant dark-store zone. The dataset includes operational and commercial measures such as order volume, average delivery time, revenue, customer rating, peak ordering period, and remaining stock.

This level of aggregation makes it possible to study product performance, delivery trends, demand concentration, and inventory status without requiring access to individual customer transactions.

Key Analytical Dimensions

- Product and SKU-level performance
- Product category
- Dark-store zone
- Date and day of the week
- Time-of-day demand band
- Inventory status
- Delivery-time performance

Key Measures

- Total orders
- Average delivery time
- Revenue
- Customer rating
- Remaining stock
- Product-level demand velocity
- Estimated days of supply
- Percentage contribution to total orders
- Percentage of records exceeding the SLA target

The synthetic nature of the dataset is intentional: it provides a controlled environment for practicing analytical methods, creating visualizations, interpreting business metrics, and developing portfolio-ready recommendations without presenting simulated results as real company data.

---

🧰 Tools & Technologies

This project focuses on Python-based data analysis and visualization.

Python

Used as the primary programming language for organizing the analysis, applying calculations, manipulating structured data, and generating reproducible results.

Pandas

Used for tabular data manipulation, grouping, aggregation, ranking, and analytical calculations. Pandas provides the foundation for transforming product-day records into business-level summaries.

NumPy

Relevant to numerical operations and analytical calculations within the broader Python data-analysis workflow.

Matplotlib

Used to create charts that communicate order distribution, delivery-time patterns, demand differences, and inventory-related findings.

CSV

Used as the structured data format for storing and loading the dataset.

Git & GitHub

Used to maintain the project repository, document the analytical workflow, and make the project accessible as part of a data analytics portfolio.

---

🔍 Analysis Modules

1. Best-Selling Product Analysis

The first module examines product-level order performance and identifies which SKUs contribute most significantly to total demand.

The analysis ranks products according to their total order volumes over the observation window. It then compares the leading product against the next-highest performer and evaluates the leading SKU's contribution to total orders.

Key findings from the synthetic dataset:

- Amul Toned Milk 500ml recorded 9,004 orders, making it the leading product in the analysis.
- Lay's Classic Chips 52g followed with 6,736 orders.
- The leading product recorded approximately 33.7% more orders than the second-place product.
- The top-selling SKU accounted for approximately 21.2% of total orders across the ten products.

These findings illustrate a hero-SKU pattern in which one product accounts for a disproportionately large share of order volume.

Business interpretation:

High-volume products require particular attention because their unavailability can affect a larger number of orders. Their demand can influence shelf placement, picking efficiency, replenishment frequency, and inventory priorities.

At the same time, order volume should not be confused with profitability. A product that generates the most orders may not necessarily generate the highest revenue or margin. A more complete commercial analysis would compare order volume, sales value, product margins, and stock availability separately.

Potential business applications:

- Prioritize high-demand SKUs during stock audits.
- Identify products that require more frequent replenishment.
- Improve product placement for faster picking.
- Compare order contribution with revenue and profitability.
- Monitor the effect of stockouts on high-volume products.

---

2. Delivery-Time Analysis & SLA Risk Monitoring

Fast delivery is central to the quick-commerce business model. An average delivery time alone, however, cannot fully explain operational performance. A zone may have an acceptable average while still experiencing frequent delays or a worsening trend.

This module examines delivery-time distribution and compares the observed delivery times with a 10-minute SLA target.

It also evaluates changes over the observation period to identify potential operational warning signals.

Key findings from the synthetic dataset:

- Overall average delivery time: 10.7 minutes.
- Product-day records exceeding the 10-minute target: 40.0%.
- Hauz Khas – Delhi showed an increase in average delivery time from 11.0 minutes to 13.0 minutes during the observation window.

Business interpretation:

The average delivery time is above the chosen target, and the proportion of records exceeding that target indicates that the issue is not limited to a single isolated observation.

The upward trend in the Hauz Khas zone provides a reason to investigate possible capacity constraints, order-packing bottlenecks, rider availability, or demand exceeding available operational resources.

These are possible explanations, not proven causes. Confirming them would require more detailed information, such as order timestamps, rider assignments, packing durations, distance, traffic conditions, and staffing levels.

Potential business applications:

- Monitor delivery performance by zone.
- Identify zones with repeated SLA breaches.
- Track rolling delivery-time averages.
- Compare high-volume zones with their delivery performance.
- Investigate recurring increases before they become persistent operational problems.
- Develop a more detailed operational dashboard for delivery teams.

Analytical principle: A trend can provide an earlier warning than a single aggregate metric, but additional operational data is needed to establish the underlying cause.

---

3. Customer Ordering Patterns: Time of Day & Day of Week

Demand is rarely distributed evenly across all hours and days. Understanding when customers place orders helps businesses plan staffing, stock availability, and fulfillment capacity more effectively.

This module examines demand across time-of-day bands and compares weekend ordering volume with average weekday demand.

Key findings from the synthetic dataset:

- The evening period, 5 PM–9 PM, accounted for approximately 41.6% of all orders.
- Weekend order volume was approximately 28.6% higher than average weekday order volume.

Business interpretation:

The evening window represents the largest ordering period in this dataset. This may reflect demand for dinner ingredients, snacks, beverages, and last-minute household purchases.

Higher weekend volume suggests that operational planning should account for differences between routine weekday demand and weekend demand.

These observations can inform resource planning, although the exact staffing levels required cannot be calculated from order shares alone. That would require information about orders per hour, preparation time, delivery capacity, and workforce availability.

Potential business applications:

- Align rider availability with peak ordering windows.
- Plan packing-staff schedules around periods of high demand.
- Prepare sufficient inventory before anticipated demand increases.
- Compare weekday and weekend category preferences.
- Evaluate whether peak-hour delivery delays coincide with higher order volumes.

The combination of time-of-day and day-of-week analysis provides two complementary perspectives: one helps plan resources within a day, while the other supports planning across the weekly operating cycle.

---

4. Dark-Store Zone Demand Analysis

Quick-commerce operations depend on distributing inventory, fulfillment capacity, and riders across multiple service areas.

If demand is concentrated in a small number of zones, those zones may require different operational priorities from areas with lower order volumes.

This module compares total orders across the five dark-store zones and identifies the zone with the highest contribution to demand.

Key finding from the synthetic dataset:

Andheri West – Mumbai recorded 15,551 orders, accounting for approximately 36.6% of total demand across the five zones.

Business interpretation:

The distribution indicates that demand is not evenly shared across the zones in the dataset.

A high-demand zone may require more frequent inventory replenishment, greater rider availability, and sufficient packing capacity. It may also deserve closer monitoring because a disruption in a heavily utilized zone could affect a relatively large portion of total order fulfillment.

The analysis also introduces the Herfindahl–Hirschman Index (HHI) as a method for measuring concentration. By squaring each zone's order-share percentage and adding the resulting values, the index provides a summary measure of how concentrated demand is across the zones.

A higher HHI indicates greater concentration, while a lower HHI indicates a more even distribution.

Potential business applications:

- Compare zone-level demand contributions.
- Identify locations that may require additional fulfillment capacity.
- Prioritize rider allocation based on demand.
- Plan replenishment frequency according to local order volume.
- Monitor the operational exposure created by demand concentration.
- Evaluate whether additional capacity or a new dark-store location deserves further investigation.

The analysis does not establish that a new dark store is necessary. Such a decision would also require geographic coverage, delivery distance, rental costs, service times, and demand forecasts.

---

5. Inventory Analysis & Stockout Risk

Inventory availability is a critical component of customer experience in quick commerce. A product may generate strong demand, but if stock is depleted before replenishment arrives, the business risks losing sales and failing to fulfill customer expectations.

This module examines the latest-day stock status and introduces inventory measures that can help identify products requiring attention.

Key findings from the synthetic dataset:

- 8 products were classified as In Stock.
- 1 product was classified as Low Stock.
- 1 product was classified as Out of Stock.
- Surf Excel Detergent was the product identified as Out of Stock.
- In total, 2 out of 10 products were at Low Stock or below.

Business interpretation:

Inventory status provides an immediate snapshot, but a static stock count does not necessarily reveal how urgently a product needs replenishment.

A product with 100 units remaining may be at greater risk than a product with 20 units remaining if its demand is substantially higher.

For this reason, the project discusses Days of Supply, which estimates how long the current inventory may last at the prevailing average daily demand rate.

It also introduces the Reorder Point, an inventory threshold at which replenishment should be initiated.

A basic reorder-point model can incorporate average demand during replenishment lead time and an additional safety-stock allowance.

Potential business applications:

- Identify products approaching inventory depletion.
- Prioritize replenishment based on demand velocity.
- Distinguish high-impact stockouts from lower-volume stockouts.
- Set product-specific inventory thresholds.
- Reduce reliance on reactive replenishment.
- Develop an automated low-stock alerting process.

Days of Supply is an estimate, not a guarantee. Actual inventory planning should account for demand variability, replenishment lead time, supplier reliability, and safety-stock requirements.

---

📈 Key Results at a Glance

The following summary brings together the main findings reported by the analysis.

Metric| Result
Average delivery time| 10.7 minutes
Delivery-time records exceeding the SLA target| 40.0%
Leading product| Amul Toned Milk 500ml
Orders for the leading product| 9,004
Leading product's share of total orders| 21.2%
Peak ordering window| 5 PM–9 PM
Share of orders during the evening window| 41.6%
Weekend order-volume lift| 28.6%
Highest-demand zone| Andheri West – Mumbai
Highest-demand zone's share| 36.6%
Products at Low Stock or below| 2 out of 10
Zone with the clearest upward delivery-time trend| Hauz Khas – Delhi
Delivery-time increase in that zone| 11.0 to 13.0 minutes

All figures above describe the synthetic dataset and the analysis period, not Zepto's verified live operational performance.

---

💡 Business Recommendations

The analysis suggests several operational actions that could be investigated in a real quick-commerce environment.

1. Prioritize High-Demand Products

Products with consistently high order volumes should receive appropriate attention during stock audits and replenishment planning. Their contribution to demand makes their availability operationally important.

2. Investigate Worsening Delivery Performance

The upward delivery-time trend in Hauz Khas should trigger a closer investigation into packing capacity, rider availability, order volume, and fulfillment delays.

3. Prepare for Evening Demand

The concentration of orders between 5 PM and 9 PM suggests that rider schedules, packing capacity, and stock readiness should be evaluated against evening demand rather than assuming equal demand throughout the day.

4. Plan for Weekend Demand Differences

Higher weekend demand may require changes to staffing and replenishment plans. The scale of any adjustment should be based on hourly order volumes and actual operating capacity.

5. Use Demand-Weighted Inventory Planning

Inventory priorities should reflect not only the remaining stock quantity but also the rate at which the product is being ordered and the time required to replenish it.

6. Monitor Zone-Level Concentration

A zone contributing a large share of total demand deserves appropriate capacity planning and contingency consideration. Demand concentration should be evaluated alongside delivery performance and inventory availability.

7. Extend the Analysis Beyond Descriptive Reporting

The current project explains observed patterns. A future version could incorporate forecasting models and automated alerts to estimate what may happen next and support earlier intervention.

---

🧠 What This Project Demonstrates

This project is designed to demonstrate more than the ability to produce charts. It shows how a beginner-level data analytics workflow can be organized around business questions and measurable outcomes.

Data Analysis Skills

- Understanding the structure and limitations of an analytical dataset.
- Working with aggregated operational records.
- Grouping data by product, date, and zone.
- Calculating totals, averages, shares, and percentage differences.
- Ranking products by order volume.
- Comparing delivery performance against a target.
- Examining temporal patterns in demand.
- Interpreting stock status and inventory risk.

Visualization & Reporting Skills

- Selecting chart types that support a specific analytical question.
- Presenting comparisons between products and zones.
- Communicating changes in delivery time.
- Highlighting peak demand periods.
- Summarizing key findings in a consistent reporting format.
- Using visual evidence to support written recommendations.

Business Thinking

- Distinguishing order volume from revenue and profitability.
- Connecting high demand with inventory planning.
- Interpreting delivery-time trends as operational warning signals.
- Understanding why aggregated averages can hide important variation.
- Recognizing the relationship between demand concentration and fulfillment risk.
- Identifying additional data required to validate possible explanations.

Analytical Communication

- Converting numerical results into understandable business findings.
- Explaining the implications of key performance indicators.
- Separating observed results from possible causes.
- Presenting recommendations with appropriate limitations.
- Documenting the dataset, assumptions, metrics, and future opportunities.

---

🔮 Future Scope: From Descriptive to Predictive Analytics

This project establishes a foundation for further analytical development.

The next stage would be to move from understanding historical patterns to estimating future outcomes.

1. Delivery-Time Forecasting

Develop a model to estimate delivery time by zone and time period using historical delivery records and relevant operational variables.

Potential inputs could include order volume, hour of day, day of week, rider availability, packing time, and distance.

The goal would be to identify potential delivery pressure before a shift begins.

2. Demand Forecasting

Build a forecasting workflow to estimate product-level demand across different zones and time periods.

Forecasts could help determine replenishment requirements, inventory thresholds, and expected peak demand.

3. Stockout-Risk Prediction

Combine inventory levels, demand velocity, and replenishment lead times to estimate which products are likely to run out of stock before new inventory arrives.

4. Anomaly Detection

Identify unusual increases in delivery time, unexpected drops in demand, or sudden changes in stock availability.

An anomaly-detection workflow could help direct operational attention toward observations that differ significantly from expected patterns.

5. Interactive Business Intelligence Dashboard

Extend the static analysis into an interactive dashboard using a BI platform such as Power BI.

Possible dashboard features include:

- Date and zone filters.
- Best-selling product rankings.
- Delivery-time KPI cards.
- SLA breach indicators.
- Time-of-day demand charts.
- Zone-level order comparisons.
- Inventory-status summaries.
- Low-stock alerts.

6. Deeper Business Analysis

Future iterations could incorporate revenue and margin comparisons, product-category trends, demand variability, and more granular delivery metrics.

These extensions would require suitable additional data and should be implemented only when the necessary fields are available.

---

📁 Suggested Repository Structure

The repository can be organized so that another learner, recruiter, or reviewer can understand the project quickly.

zepto-quick-commerce-analysis/
│
├── README.md
│
├── data/
│   └── zepto_order_data.csv
│
├── notebooks/
│   └── zepto_quick_commerce_analysis.ipynb
│
├── reports/
│   └── Zepto_Quick_Commerce_Data_Analysis.pdf
│
├── visuals/
│   ├── best_selling_products.png
│   ├── delivery_time_analysis.png
│   ├── order_patterns.png
│   ├── zone_demand_analysis.png
│   └── inventory_stockout_risk.png
│
└── requirements.txt

This is a suggested structure. File names should be adjusted to match the files actually committed to the repository.

---

🚀 How to Explore the Project

1. Clone or download the repository.
2. Review the README to understand the objectives, dataset, and business questions.
3. Open the analysis notebook, if included.
4. Install the required Python libraries.
5. Load the dataset and follow the analytical steps.
6. Examine the generated visualizations.
7. Compare the reported findings with the calculations in the notebook.
8. Review the business recommendations and the limitations of the analysis.

Example Environment Setup

git clone <your-repository-url>
cd zepto-quick-commerce-analysis

Install the relevant libraries:

pip install pandas numpy matplotlib seaborn jupyter

Launch Jupyter Notebook:

jupyter notebook

These commands are illustrative setup instructions. The repository should include the corresponding notebook, dataset, and dependency list for the workflow to run as documented.

---

⚠️ Limitations & Responsible Interpretation

This project has several limitations that should be considered when interpreting its results.

- Synthetic data: The dataset is generated for practice and does not represent verified live Zepto order data.
- Limited observation period: The analysis covers 15 days, which is insufficient to establish long-term seasonal patterns.
- Aggregated records: Product-day summaries do not expose every individual order, delivery journey, or customer interaction.
- Limited operational variables: The dataset does not independently establish the causes of delivery delays.
- Inventory estimates: Days of Supply and reorder-point calculations depend on demand and replenishment assumptions.
- Descriptive scope: The findings identify patterns but do not establish causation or guarantee future performance.
- Business recommendations: Recommendations are analytical suggestions that would require validation against real operational constraints before implementation.

These limitations are an important part of the project. Sound analysis requires not only identifying patterns but also understanding what the available data can and cannot support.

---

📚 References & Learning Resources

The project draws on the following learning resources and tools:

- Pandas Documentation: https://pandas.pydata.org/docs/
- NumPy Documentation: https://numpy.org/doc/
- Matplotlib Documentation: https://matplotlib.org/stable/
- Seaborn Documentation: https://seaborn.pydata.org/
- GitHub Documentation: https://docs.github.com/

The dataset used for the project is synthetic and was identified in the accompanying report as AI-generated.

---

👨‍💻 About This Project

This project is part of my learning journey in Data Analytics, Python, and Business Intelligence.

Through this work, I am practicing how to approach business problems systematically, work with structured datasets, calculate meaningful metrics, create visualizations, and communicate findings in a way that connects data with operational decisions.

My focus is not only on learning analytical tools but also on developing the habit of asking better business questions, validating results, documenting assumptions, and explaining what the numbers actually mean.

This repository represents a practical step toward building stronger skills in data analysis, exploratory data analysis, data visualization, and business-oriented problem-solving.

---

🏁 Final Summary

Zepto Quick Commerce Data Analysis brings together five connected areas of operational analytics: product performance, delivery-time monitoring, customer ordering patterns, regional demand concentration, and inventory risk.

Using a synthetic dataset of 150 product-day records across ten products and five dark-store zones, the project demonstrates how structured data can be transformed into measurable findings and potential business actions.

The analysis identifies a leading SKU, a delivery-time trend requiring investigation, a peak evening ordering window, an uneven distribution of demand across zones, and products requiring inventory attention.

More importantly, it illustrates the role of an analyst in moving beyond raw numbers: defining the right questions, selecting appropriate metrics, interpreting results carefully, recognizing limitations, and communicating findings clearly.

The next step is to extend this foundation into more advanced analytical work, including demand forecasting, delivery-time prediction, automated anomaly detection, and interactive dashboards.

The goal is simple: turn data into understanding, turn understanding into actionable insight, and build a stronger foundation for data-driven decision-making.

---

🏷️ Topics

"data-analytics" "python" "pandas" "numpy" "matplotlib" "seaborn" "exploratory-data-analysis" "descriptive-analytics" "quick-commerce" "zepto" "business-analytics" "data-visualization" "inventory-analysis" "demand-analysis" "delivery-performance" "supply-chain-analytics" "github-portfolio" practice.