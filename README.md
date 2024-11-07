# LITA_PROJECTS-Customer Data

This repository will contain detailed information about my Customer Data -project analyses and visualizations.

## PROJECT TITLE: Customer Data

### Project Overview 
---
This Data Analysis Project aims to generate insight into the subscription patterns and revenue generated from the customers of an organization over the past 2 years. Analysing the paramaters in the data, I sought to gather enough insight to make reasonable decisions, enabling me to tell a compelling story around the data from the insight gotten and to determine the best performance from the data.
---
### Tables of Content
[Data Sources](#Data-Sources)

[Data Collected](#Data-Collected)

[Tools used](#Tools-used)

[Data Cleaning and Preparation](Data-Cleaning-and-Preparation)

[Exploratory Data Analysis.](Exploratory-Data-Analysis.)

[Data Analysis](Data-Analysis-Visual-Analysis-and-Inference)

[Visual Analysis and Inference](Visual-Analysis-and-Inference)

[Recommendations](Recommendations)

---

### Data Sources

The primary source of data used is an Excel datasheet provided by the LITA Data Analysis Team.

### Data Collected 

1. Customer Id: A unique identifier assigned to a customer, it helps in efficient customer management and tracking
2. CustomerName: This is used to identify and address individual customers.
3. Subscription Type: The terms and conditions of a customer's recurring payment or service agreement.
4. Region: The geographical area where the business operates.
5. Subscription Start: The date when a customer's subscription becomes active.
6. Subscription End:  The date when a customer's subscription becomes terminated.
7. Revenue: The income generated by a business from its normal operations, such as sales of a product or service.

### Tools used
- Microsoft Excel for Data
-  Cleaning, Analysis and Visualization.
- Structured Query Language - SQL for Querying of data.
- Power Bi for Visualization.
- GitHub for Portfolio Building

### Data Cleaning and Preparation.
After obtaining the dataset, the following action was performed;
1. Data Loading and Inspection.
2. Handling missing variables.
3. Data Cleaning and Formatting.

### Exploratory Data Analysis.
EDA involved the exploring of the data to answer some questions about the data;
- What is the total number of customers from each region?
- The most popular subscription type by the number of customers.
- The average subscription duration for all customers.
- The total revenue by subscription type.
- The top 3 regions by subscription cancellations.
- The total number of active and canceled subscriptions.
It provides insight into subscription trends, subscription type popularity, and customer behaviour.

### Data Analysis
These are some of the codes, queries and formula used in the course of the analysis;

```SQL
SELECT Region, COUNT(DISTINCT CustomerID) AS Total_Customers FROM `customer data` GROUP BY Region; 

SELECT CustomerID FROM `customer data` WHERE SubscriptionEnd IS NOT NULL AND DATEDIFF(SubscriptionEnd,SubscriptionStart) <= 180; 

SELECT CustomerID FROM `customer data` WHERE SubscriptionEnd IS NOT NULL AND DATEDIFF(SubscriptionEnd,SubscriptionStart) > 365;

```

```EXCEL
SUBSCRIPTION DURATION = SubscriptionEnd - SubscriptionStart.

```

### Visual Analysis and Inference


![Customer Data Excel](https://github.com/user-attachments/assets/830e2159-1f68-4cdb-b3b6-bedf05b91810)


![Customer Data Excel (7)](https://github.com/user-attachments/assets/ac3d784a-4cd3-4bc5-bc2c-30be004ae889)


![Customer Data Excel (6)](https://github.com/user-attachments/assets/61578f35-b222-47b9-818e-adbe6026d9e0)


![Customer Data Excel (5)](https://github.com/user-attachments/assets/3a1e1e3c-cb9b-4ebe-8ba9-85b8640e962f)


![Customer Data Excel (4)](https://github.com/user-attachments/assets/db0b6ba6-aca4-4da5-9eba-a7e8140fe7a1)


![Customer Data Excel (3)](https://github.com/user-attachments/assets/e6c778a6-1728-4fef-ad4d-903beae09124)


![Customer Data Excel (2)](https://github.com/user-attachments/assets/4511eb4b-ce34-455f-a970-a5a73f91562b)


![Screenshot (70)](https://github.com/user-attachments/assets/b58cc828-e4d1-41aa-a664-128cc347be44)


![Customer Data SQL](https://github.com/user-attachments/assets/1ead5cad-01f3-4519-88fe-45ba9efe7b9f)


![Customer Data SQL (5)](https://github.com/user-attachments/assets/3092bfa5-e9ea-4a89-ad5f-9d3c6c4c052a)


![Customer Data SQL (4)](https://github.com/user-attachments/assets/922f4086-d51e-4866-bdb5-bd92e5efcf77)


![Customer Data SQL (3)](https://github.com/user-attachments/assets/dc9bae40-9ca3-4d31-98fe-fc43d71226dc)


![Customer Data SQL (2)](https://github.com/user-attachments/assets/07513478-4a37-4e0b-ba45-d423fd667303)


![Screenshot (73)](https://github.com/user-attachments/assets/12c2444e-4a4b-4820-a7fb-240ac5a5103c)


![Screenshot (72)](https://github.com/user-attachments/assets/2c3f897e-1ac2-42de-9bb8-5edcb99c3c59)



#### Inference.

The analysis revealed that the most popular subscription type is the Basic plan, with the Standard plan being the least popular. 
The Basic subscription generated the highest revenue at #8,103,240. 
Preferences varied by region: the East and North regions favored the Basic subscription, 
while the South and West leaned towards the Premium and Standard subscriptions, respectively.

Across board, more people cancelled 
their subscriptions in all regions except the East where the fewest 
people cancelled their subscription.

In particular, the North had the highest number of cancellations (5,067), slightly more than the South (5,064) and West (5,044).

In terms of revenue, the East led with #16,958,763, followed by the South at #16,899,064, the West at #16,864,376, and the North at #16,817,972.

The average subscription duration across all regions was calculated to be 369.92 days. 


### Recommendations.

1. Enhance Marketing for the Basic Subscription: Since the Basic subscription is the most popular, it could be beneficial to further promote it, especially in the regions where it’s already favored (East and North). Maintaining and enhancing the Basic subscription plan's features and pricing - Offering special deals or discounts could help boost its appeal and attract more customers.

2. Add value to the Standard Subscription: The Standard subscription is the least popular, indicating that it may not be meeting customer expectations. Consider conducting a customer survey to identify why this plan is less appealing, and possibly redesign it with added benefits or a more competitive pricing structure.
  
3. Region-Specific Marketing Strategies:
   - South and West Regions: These regions prefer the Premium and Standard plans, incorporating targeted marketing that emphasizes the unique benefits of these plans could increase retention and reduce cancellations.

   - North Region: With the highest number of cancellations, it might be worthwhile to analyze the feedback from customers in this region. Implement a customer retention strategy: Improve customer support, offer flexible payment options, and incentives - Consider offering discounts or promotions to customers in the North region.
  
4. Develop a Cancellation Prevention Program: Across all regions, cancellations appear to be significant. Focus on customer engagement and support - Consider implementing an automated system to identify customers who are likely to cancel (e.g., based on low engagement) and offering them special promotions or customer support to help address any issues. Implement a loyalty program or rewards for long-term subscribers.

5. Extend Average Subscription Duration: With an average subscription duration of around 370 days, consider strategies to increase this metric. Offer annual subscription discounts, multi-year plans, or loyalty rewards for long-term subscribers to encourage customers to remain subscribed longer.

7. Analyze Revenue Patterns: Revenue is strong across regions, hence, look into which specific features or benefits drive the highest sales within each plan. This insight could help to replicate successful features in other plans or improve underperforming ones like the Standard subscription.
