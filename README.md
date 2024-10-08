# TECO Customer Churn Analysis

Dashboard Link: https://github.com/Exagged/Customer-Churn-Analysis

### Problem Statement:

This dashboard helps TECO understand and predict customer churn more effectively. It identifies key factors contributing to churn and allows the company to take action in retaining customers. Through detailed metrics such as churn rates, customer tenure, contract type, payment method, and monthly charges, this dashboard provides a comprehensive view of customer behavior. It also helps segment customers based on their likelihood of churn, providing insights into retention strategies.

The analysis reveals that customers with shorter tenures, month-to-month contracts, and higher monthly charges are more likely to churn. By using this dashboard, TECO can focus on these segments, optimizing marketing and customer service strategies to minimize churn and increase customer retention.

### Steps Followed

- Step 1: Data Loading
    
    The data was loaded into Power BI Desktop from a CSV file containing TECO’s customer churn data. The dataset included various fields such as customer demographics, contract details, service usage, and whether the customer churned.

- Step 2: Data Profiling
    
    The data was cleaned and transformed in the Power Query Editor. Column profiling based on the entire dataset was enabled to inspect data quality, ensuring no significant missing values, especially in crucial fields like customer tenure, contract type, and monthly charges.

- Step 3: Handling Missing Values

    Missing or empty values in fields like payment method were identified. Data transformations were applied, replacing missing values or removing rows where necessary to maintain the integrity of the dataset.

- Step 4: Creating Calculated Fields

    Calculated columns were added to better understand customer behavior. For example, a "Customer Tenure" column was created to group customers based on their length of service, and a "Churn Probability" measure was calculated using logistic regression analysis.

- Step 5: Visual Customization

    In the report view, a clean and visually engaging theme was selected. The dashboard was designed to be intuitive, with colors representing churn (red for churn, green for retained). This allowed for an easy-to-navigate interface to quickly draw insights.

- Step 6: Building Slicers for Interactivity

    Slicers were added for fields like "Contract Type," "Payment Method," and "Monthly Charges" to allow users to filter the data dynamically and explore different segments. This enabled real-time insights into customer churn by specific categories.

- Step 7: Card Visuals for Key Metrics

    Important metrics were displayed using card visuals, including:

        Total Customers
        Total Churn Rate
        Average Monthly Charges
        Average Tenure
- Step 8: Churn Rate by Segment

    A bar chart was created to show churn rate by contract type, revealing that customers with month-to-month contracts had the highest churn rates. A similar analysis was done for payment method, showing that customers paying via electronic check were more likely to churn.

- Step 9: Customer Segmentation by Tenure

    A line chart was used to analyze customer churn across different tenure groups. Customers with shorter tenures (less than 12 months) showed significantly higher churn rates compared to long-term customers.

- Step 10: Churn Rate by Monthly Charges

    A scatter plot was used to show the relationship between monthly charges and churn. It was observed that customers with higher monthly charges tended to have higher churn rates, suggesting the need for targeted retention offers.

- Step 11: Geo Visualization

    A map visualization was used to display churn by geographic region, helping TECO identify areas with higher churn rates and prioritize interventions in those regions.

- Step 12: Creating Churn Prediction Model

    A logistic regression model was built to predict the likelihood of churn based on factors such as tenure, contract type, and payment method. The results were displayed in the dashboard using a gauge visual that shows the predicted churn probability for any given customer.

- Step 13: Insights on Payment Method
    
    A pie chart was created to show the distribution of customers by payment method, highlighting that electronic check users are at higher risk of churn. This insight provides an opportunity for TECO to explore alternative payment options or incentives for these customers.

- Step 14: Contract Analysis

    Another key insight came from analyzing contract types. A donut chart was used to visualize that month-to-month contracts accounted for the majority of churn, while long-term contracts (1 year and 2 years) had significantly lower churn rates.

- Step 15: Custom DAX Measures

    Several DAX measures were created, such as:

        Churn Rate = CALCULATE(COUNTROWS(Customer Data), Customer Data[Churn] = "Yes") / COUNTROWS(Customer Data)
        
        Average Monthly Charges = AVERAGE(Customer Data[Monthly Charges])
        
        Customer Tenure Groups = IF(Customer Data[Tenure] <= 12, "Short Term", IF(Customer Data[Tenure] <= 36, "Medium Term", "Long Term"))

These measures helped in accurately analyzing customer behavior and were used in various visuals throughout the dashboard.

- Step 16: Insights on Service Types

    A bar chart was added to compare churn rates by service type. Customers subscribed to fiber internet services had a higher churn rate compared to those using DSL, allowing TECO to focus on service improvements or bundle offers to reduce churn in this segment.

- Step 17: Publishing the Dashboard

    The final dashboard was published to Power BI Service, enabling the team to share it with stakeholders for real-time access and updates. The interactive features allowed team members to filter the data and explore churn trends based on their own criteria.

# Insights

[1] Total Customers Analyzed = 7,043

    - Churn Rate: 26.53% of customers have churned, indicating that about one in four customers have discontinued their services.

    - Tenure Impact: Customers with shorter tenures (1-2 months) show the highest churn rates, while those with longer tenures (above 24 months) tend to stay longer.

[2] Monthly Charges Influence

    - Churn Distribution by Monthly Charges: The average monthly charge for all customers is $64.76, with churned customers averaging $74.20 in monthly charges, compared to $61.20 for non-churned customers.

    - High-Risk Segment: Customers paying over $80 per month have a churn rate of 40%, while those paying less than $40 per month have a significantly lower churn rate of 10%.
    
[3] Payment Method Insights

    - Electronic Check Risk: Electronic check users exhibit the highest churn rate at 42%, compared to other payment methods like bank transfers and credit cards, which have churn rates below 15%. 

    - This suggests that customers using electronic checks might experience a less satisfactory payment process.

[4] Contract Type Analysis

    - Contract-Based Churn: 73% of churned customers have month-to-month contracts, while only 11% have a one-year contract and 16% have a two-year contract. 

    - Long-term contracts are associated with greater customer retention.

    - Paperless Billing Impact: 59% of customers who churned were using paperless billing, suggesting a potential area for improving customer engagement with digital payment methods.

[5] Churn Prediction Model
    - Predicted Churn Probability: Based on the logistic regression model, customers with the following characteristics have the highest probability of churn: month-to-month contracts, electronic check payment method, tenure of less than 12 months, and higher monthly charges.

    - Senior Citizen Impact: 45% of senior citizens with month-to-month contracts have a higher likelihood of churn compared to younger customers.

[6] Regional Analysis

    - Churn by Region: The Southern region accounts for 35% of the total churn, making it a key area for targeted retention strategies. The Northern region shows the lowest churn rate at 12%.

    - Internet Service Insight: Fiber optic customers have a churn rate of 30%, significantly higher than DSL customers, who have a churn rate of 18%. 

    - This indicates that satisfaction levels with fiber optic service may need attention.

[7] Service-Based Churn Insights
    
    - Online Services: Customers without online security, backup, or tech support are more likely to churn. For instance, the churn rate among customers without online security is 45%.

    - Streaming Services: Customers with streaming services like StreamingTV and StreamingMovies have a slightly higher churn rate, suggesting a need to review bundled service offerings to improve retention.
