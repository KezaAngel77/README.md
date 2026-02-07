## PROBLEM DEFINITION

**Business Context**

This project examines a retail company operating in the consumer goods industry. The analysis is conducted within the sales department, which is responsible for tracking product performance and customer purchasing behavior.

**Data Challenge**

The company stores large volumes of transactional sales data, but the raw tables do not provide meaningful analytical insights. Management lacks visibility into sales rankings, trends over time, and customer performance segmentation.

**Expected Outcome**

The analysis aims to produce actionable insights that support decision-making, including identifying top-performing products, understanding sales trends, and segmenting customers based on purchasing behavior.

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

b) **Products**: Contains product details such as product identifier, product name, and unit price.

c) **Sales**: Records transactional data, including sale identifier, customer identifier, product identifier, sale date, quantity sold, and total sales amount.

The Customers and Products tables have one-to-many relationships with the Sales table through foreign key constraints.

## JOIN BUSINESS INTERPRETATIONS

**INNER JOIN**

This query retrieves records where customers, products, and sales transactions match across tables. It enables analysis of valid sales activity involving existing customers and available products.

**LEFT JOIN**

This query returns all customers, including those without any sales transactions. It helps identify inactive customers who may require targeted engagement or marketing strategies.

**RIGHT JOIN / FULL JOIN**

This query highlights products that have not been sold. It supports identification of underperforming or inactive products within the inventory.

**FULL OUTER JOIN**

This query combines all customers and products, including matched and unmatched records. It provides a comprehensive overview of active and inactive entities within the database.

**SELF JOIN**

This query compares records within the same table to identify similarities, such as customers located in the same region or transactions occurring within the same time period.

## WINDOW FUNCTIONS

**Ranking Window Functions**

Ranking functions are used to order customers or products based on sales performance. This allows the identification of top performers and supports performance-based evaluation.

**Aggregate Window Functions**

Aggregate window functions calculate cumulative and average values while preserving individual rows. They are useful for analyzing running totals and observing trends over time.

**Navigation Window Functions**

Navigation functions such as LAG() and LEAD() enable comparisons between current and previous periods. This supports the analysis of growth patterns and sales fluctuations.

**Distribution Window Functions**

Distribution functions divide customers into performance-based groups. This segmentation assists in targeted decision-making and customer management strategies.

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
