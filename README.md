# Telco Churn Analysis

## Table of Contents

- [Project Summary](#project-summary)
- [Dashboard](#dashboard)
- [Data Tools](#data-tools)
- [Key Trends and Patterns](#key-trends-and-patterns)
- [Recommendation](#recommendation)
- [Conclusion](#conclusion)

### Project Summary

This project focuses on analyzing customer churn for a subscription-based service, aiming to identify key trends, patterns, and predictors of churn to inform retention strategies. Leveraging a comprehensive dataset, the analysis uncovers critical insights into customer demographics, behaviors, and service usage, segmented across various dimensions such as gender, contract type, tenure, and more.

### Dashboard

![Screenshot 2025-04-24 130938](https://github.com/user-attachments/assets/cb4a64cf-aa0f-469d-9b47-b0d8f57e862d)![Screenshot 2025-04-24 131034](https://github.com/user-attachments/assets/5eb6093b-0ff6-4acf-9279-d7476e7481ba)![Screenshot 2025-04-24 131256](https://github.com/user-attachments/assets/a9901f53-2c83-4120-bbc7-6278933453ce)![Screenshot 2025-04-24 131348](https://github.com/user-attachments/assets/c2880fbd-25c9-4f5f-bbec-0ffe95ec3e65)



### Data Tools

- Excel - For Cleaning, missing values, and duplicates were addressed to ensure data quality. Excel’s filtering, sorting, and formula capabilities enabled efficient preprocessing, preparing the data for deeper analysis
- SQL - Used to perform advanced querying, aggregations, and statistical analysis, as well as to build a churn prediction model. SQL’s ability to handle large datasets and perform complex joins allowed for detailed segmentation and trend analysis.
- Power BI - Used to create a dynamic dashboard, providing an intuitive and interactive visualization of the findings, enabling stakeholders to explore trends and patterns effortlessly.

### Key Trends and Patterns

#### 1.  Overall Churn Metrics
- The total customer base is 7,043, with 1,869 customers having churned, resulting in a churn rate of 26.5%.
- The average tenure is 32 months, with average monthly charges of $64.76 and average total charges of $2,280.
- Of the 1,869 churners, 939 are female (50.24%) and 930 are male (49.76%), indicating a near-even gender distribution among churners. However, the churn rate among females (26.2%) is slightly lower than males (26.9%).
- Customers with partners are less likely to churn (669 churners) compared to those without (1,200 churners). Similarly, customers with dependents churn less frequently (106 churners) than those without (1,763 churners).
- Churn rates vary significantly by city, with Acampo showing the highest churn rate at 78.8%, while cities like Acton and Alamo have 0% churn rates.
- Payment methods also influence churn: customers using electronic checks have the highest churn rate (45.3%), while those using credit cards (automatic) have the lowest (15.2%).
- Churn reasons highlight competitors (621 churners), service dissatisfaction (493), and attitude (327) as the top drivers of churn.
- Internet service type impacts churn: fiber optic users have a 41.9% churn rate, compared to DSL (19.0%) and those with no internet service (7.4%).
- Tenure analysis shows that newer customers (0–6 months) have the highest churn rate (52.9%), which decreases as tenure increases, dropping to 11.9% for customers with 3+ years of tenure.
- Services like tech support, streaming movies, and streaming TV show higher churn rates when not subscribed to (e.g., 46.7% for no streaming movies vs. 14.5% for subscribers).

#### 2.  Demographic Insights
- Churn among senior citizens is slightly higher (1,393 churners) than non-seniors (476 churners), though the senior citizen group is smaller, indicating a higher churn rate in this demographic.
- Cities like Los Angeles (90 churners) and San Diego (81 churners) have the highest absolute churn numbers, reflecting larger customer bases, but smaller cities like Acampo have disproportionately high churn rates.
- Average monthly charges increase with tenure, peaking at $96.80 for customers with 60–70 months of tenure, but churners generally have lower average charges ($41.91 for 0–10 months) compared to non-churners ($59.52).

#### 3.  Customer Segmentation 
- Contract type significantly impacts churn: month-to-month contracts have the highest churn rate (3,875 churners), compared to two-year (1,665) and one-year (1,473) contracts.
- Internet service analysis reinforces the trend: fiber optic users (3.1K churners) are more likely to churn than DSL (2.4K) or those without internet (1.5K).
- Churn reasons align with the overview, with competitors (193 churners) and price dissatisfaction (154) being prominent.
- Average monthly charges for churners ($74.44) are higher than for non-churners ($61.27), suggesting that price sensitivity may drive churn.
- Scatter plots of customers by basic services, new customers by high potential, and loyal customers show that month-to-month contract holders consistently have higher churn across all segments, with loyal customers (longer tenure) showing lower churn rates.

#### 4.  Churn Prediction
- The prediction model identifies 204 customers at high risk of churning, with detailed metrics such as monthly charges, average monthly spending, and total charges.
- Predicted churners have higher monthly charges (e.g., $90.35 for customer 0139-IVF6G) compared to the overall average ($64.76), reinforcing the link between cost and churn.
- Tenure analysis of predicted churners shows a peak at 3–4 months (28 customers), indicating that early-stage customers are most at risk.
- Tech support and multiple lines significantly influence churn risk: customers without tech support (164 predicted churners) and with multiple lines (126 predicted churners) are more likely to churn.
- Payment method trends mirror the overview, with electronic check users (135 predicted churners) being the most at-risk group.

  ### Recommendation

#### 1. Incentivize Longer-Term Contracts
- Insight: The analysis shows that customers on month-to-month contracts have a significantly higher churn rate (3,875 churners) compared to those on one-year (1,473 churners) or two-year contracts (1,665 churners). Additionally, churn rates drop as tenure increases—52.9% for 0–6 months versus 11.9% for 3+ years.
- Strategy: Encourage customers to switch to longer-term contracts by offering incentives such as discounted rates, free add-on services (e.g., streaming movies or tech support), or waiving setup fees for one- or two-year commitments. For example, a 10% discount on monthly charges for customers who sign a one-year contract could reduce the flexibility-related churn seen in month-to-month plans. Additionally, create a loyalty program that rewards customers with benefits as their tenure grows, further incentivizing them to stay beyond the initial 6 months.

#### 2. Improve Fiber Optic Service Experience
- Insight: Customers using fiber optic internet have a high churn rate of 41.9%, compared to DSL (19.0%) and those with no internet service (7.4%). This suggests potential issues with service quality, reliability, or pricing for fiber optic users.
- Strategy: Conduct a root cause analysis to identify why fiber optic users are churning at such a high rate. This could involve surveying customers to understand their pain points—whether it’s network reliability, speed, or cost. If pricing is the issue (noting that churners have higher average monthly charges of $74.44), consider introducing tiered pricing plans that offer more affordable options. If service quality is the problem, invest in infrastructure improvements and proactive maintenance to reduce outages. Offering a satisfaction guarantee or a free month of service for any reported issues could also rebuild trust among fiber optic users.

#### 3. Enhance Onboarding and Early Engagement
- Insight: The churn rate is highest among new customers (52.9% for 0–6 months), and the prediction model highlights a peak of predicted churners at 3–4 months (28 customers).
- Strategy: Focus on improving the onboarding experience to reduce early churn. Implement a structured onboarding program that includes a welcome package, personalized setup assistance, and a dedicated support contact for the first 90 days. Follow up with customers at the 1-month and 3-month marks to address any concerns and ensure they’re satisfied with the service. Offering a small discount or bonus (e.g., a free month of streaming movies) for completing a feedback survey at these intervals can also increase engagement and help identify issues early.

#### 4. Promote Automatic Payment Methods
- Insight: Customers using electronic checks have the highest churn rate (45.3%), while those using automatic credit card payments have the lowest (15.2%). This trend is also evident in the prediction model, with 135 predicted churners using electronic checks.
- Strategy: Encourage customers to switch to automatic payment methods like credit cards or bank transfers by offering incentives such as a one-time discount or entry into a prize draw. Simplify the process of setting up automatic payments through an easy-to-use online portal or app, and provide clear communication about the benefits, such as convenience and reduced risk of late payments. For customers using electronic checks, send reminders about the benefits of switching and offer assistance in transitioning to a more stable payment method.

#### 5. Expand Access to Support Services
- Insight: Customers without tech support have a high churn rate (46.7% vs. 14.5% for subscribers), and the prediction model identifies 164 customers without tech support as at-risk. Similarly, services like streaming movies and TV show higher churn rates when customers don’t subscribe (e.g., 46.7% for no streaming movies).
- Strategy: Make tech support more accessible by offering it as a free or low-cost add-on for the first year, especially for new customers. Train support staff to proactively reach out to customers who haven’t opted for tech support, offering a free trial to demonstrate its value. For streaming services, bundle them with internet plans at a discounted rate to increase adoption since subscribers to these services are less likely to churn. For example, a “welcome bundle” that includes internet, streaming movies, and tech support at a reduced rate for the first 6 months could encourage uptake and reduce churn.

#### 6. Address Regional Churn Disparities
- Insight: Churn rates vary significantly by city, with Acampo showing a 78.8% churn rate, while cities like Acton and Alamo have 0% churn.
- Strategy: Conduct a regional analysis to understand the drivers of churn in high-churn areas like Acampo. This could involve assessing competition, service quality, or customer demographics in these regions. In high-churn areas, deploy targeted retention campaigns such as localized promotions, community events, or partnerships with local businesses to strengthen brand loyalty. For example, offering a “loyalty discount” to customers in Acampo who stay for 12 months could help reduce churn. Conversely, study the factors contributing to 0% churn in cities like Acton and replicate those strategies in other regions.

#### 7. Tackle Top Churn Reasons
- Insight: The top reasons for churn include competitors (621 churners), service dissatisfaction (493), and attitude (327).
- Strategy: Address these churn drivers directly:
  - Competitors: Conduct a competitive analysis to understand what competitors are offering (e.g., better pricing, faster internet, or additional services). Match or exceed these offerings where feasible, such as by introducing a price-match guarantee or enhancing service features.
  - Service Dissatisfaction: Improve service reliability and customer support response times. Implement a proactive monitoring system to detect and resolve service issues before customers complain, and follow up with affected customers to ensure satisfaction.
  - Attitude: Train customer facing staff to improve interactions, focusing on empathy and problem-solving. Introduce a feedback loop where customers can easily share their experiences, and use this feedback to address attitude related issues.

#### 8. Target At-Risk Customers with Personalized Offers
- Insight: The prediction model identifies 204 customers at high risk of churning, with higher monthly charges (e.g., $90.35 for customer 0139-IVF6G) compared to the overall average ($64.76).
- Strategy: Use the prediction model to proactively target at-risk customers with personalized retention offers. For example, offer a temporary discount on monthly charges for customers with high bills, or provide a free upgrade to a service they don’t currently have (e.g., streaming TV). Contact these customers directly via email or phone with a tailored message, such as: “We’ve noticed you might be considering leaving let us make it right with a 20% discount for the next 3 months.” This proactive approach can make customers feel valued and reduce their likelihood of churning.


### Conclusion
These retention strategies are directly informed by the churn analysis, addressing the most significant drivers of customer attrition. By focusing on longer-term contracts, improving service quality, enhancing onboarding, promoting automatic payments, expanding support access, addressing regional disparities, tackling churn reasons, and targeting at-risk customers, the company can significantly reduce its 26.5% churn rate. Implementing these strategies will not only improve customer satisfaction but also enhance long-term profitability by fostering a more loyal customer base.
