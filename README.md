NAMES: KAYITARE Keza Angel.

Student ID: 29178.

## PROBLEM DEFINITION

**Business Context**

This project examines a retail company operating in the consumer goods industry selling electronics. The analysis is conducted within the sales department, which is responsible for tracking product performance and customer purchasing behavior.

**Data Challenge**

The company stores sales transactions in multiple related tables, making it difficult to analyze performance using raw data alone. Without advanced SQL techniques, management cannot easily identify top-selling products, customer activity levels, or sales trends over time.

**Expected Outcome**

The analysis is expected to provide insights into product performance, customer purchasing behavior, and sales trends. These insights will support data-driven decisions such as improving product offerings, targeting customers effectively, and optimizing sales strategies.

## SUCCESS CRITERIA

The project is guided by the following five measurable success criteria:
1. Identify top-performing products based on total sales using ranking window functions such as RANK().
2. Calculate running sales totals over time using aggregate window functions such as SUM() OVER().
3. Analyze month-to-month sales changes using navigation window functions like LAG().
4. Segment customers into four performance groups using distribution window functions such as NTILE(4).
5.Compute moving average sales trends to evaluate short-term performance using AVG() OVER().

## DATABASE SCHEMA DESCRIPTION

The database is composed of three related tables designed to support retail sales analysis:

a) **Customers**: Stores customer information, including customer identifier, name, and region.

![Customers table](https://github.com/user-attachments/assets/b78b7a42-02e3-42a0-8c12-75543bf3ed06)


b) **Products**: Contains product details such as product identifier, product name, and unit price.

![Products table](https://github.com/user-attachments/assets/8054d98e-52f6-4211-9b64-fdf2c7d2a98c)


c) **Sales**: Records transactional data, including sale identifier, customer identifier, product identifier, sale date, quantity sold, and total sales amount.

![Sales table](https://github.com/user-attachments/assets/b61f4921-5dba-4c97-87aa-de9092f82335)


The Customers and Products tables have one-to-many relationships with the Sales table through foreign key constraints.

![ER Diagram](https://github.com/user-attachments/assets/760bd872-76c5-45c0-be88-2789779c25a9)


## JOIN BUSINESS INTERPRETATIONS

**INNER JOIN**

This query retrieves records where customers, products, and sales transactions match across tables. It enables analysis of valid sales activity involving existing customers and available products.

![Inner Join](https://github.com/user-attachments/assets/54de9ad8-8edf-4c4a-9d36-d5b8fd0413dc)


**LEFT JOIN**

This query returns all customers, including those without any sales transactions. It helps identify inactive customers who may require targeted engagement or marketing strategies.

![Left Join](https://github.com/user-attachments/assets/018384b4-cdaf-4259-b98d-215ea323bb2f)


**RIGHT JOIN / FULL JOIN**

This query highlights products that have not been sold. It supports identification of underperforming or inactive products within the inventory.

![Right Join](https://github.com/user-attachments/assets/9f148eb7-f193-44b2-afd1-0e42fd2a4681)


**FULL OUTER JOIN**

This query combines all customers and products, including matched and unmatched records. It provides a comprehensive overview of active and inactive entities within the database.

![Full Join](https://github.com/user-attachments/assets/5ac8dd4d-d4d5-41d2-9ade-4ace9dc77377)


**SELF JOIN**

This query compares records within the same table to identify similarities, such as customers located in the same region or transactions occurring within the same time period.

![Self-Join](https://github.com/user-attachments/assets/36c3a47e-c41f-43ba-966d-4e360d8aa60c)


## WINDOW FUNCTIONS

**Ranking Window Functions**

Ranking functions are used to order customers or products based on sales performance. This allows the identification of top performers and supports performance-based evaluation.

![Ranking window function ](https://github.com/user-attachments/assets/eb3aa4ba-b5bd-4156-bdf0-dd8c6a18e962)


**Aggregate Window Functions**

Aggregate window functions calculate cumulative and average values while preserving individual rows. They are useful for analyzing running totals and observing trends over time.

![Aggregate Window Function](https://github.com/user-attachments/assets/ec63fdd6-3436-4953-9643-e6b94ffbbf59)


**Navigation Window Functions**

Navigation functions such as LAG() and LEAD() enable comparisons between current and previous periods. This supports the analysis of growth patterns and sales fluctuations.

![Navigation Window Function](https://github.com/user-attachments/assets/c290e98a-e3a4-436b-942e-73c7e70dfc9c)


**Distribution Window Functions**

Distribution functions divide customers into performance-based groups. This segmentation assists in targeted decision-making and customer management strategies.

![Distribution Window Function](https://github.com/user-attachments/assets/1848c55a-f878-4b02-b1c1-f79052b76a15)


shell
## RESULTS ANALYSIS

 **Descriptive Analysis**
 
The analysis reveals differences in product sales performance and customer purchasing behavior over time. Certain products and customers consistently generate higher revenue than others.

**Diagnostic Analysis**

Variations in sales performance are influenced by factors such as customer purchasing frequency, product pricing, and demand patterns. Period-to-period comparisons indicate fluctuations in sales activity.

**Prescriptive Analysis**

The business should prioritize high-performing products, re-engage inactive customers, and review strategies for underperforming items. Data-driven actions can improve overall sales outcomes.

## KEY INSIGHTS
1. A limited number of products contribute significantly to total sales revenue.
2. Customer segmentation reveals varying purchasing behaviors across different regions.

## REFERENCES
Official SQL documentation and reputable database learning resources were consulted for this project.

All sources were properly cited. The implementations and analysis represent original work. No AI-generated content was copied without attribution or adaptation.
