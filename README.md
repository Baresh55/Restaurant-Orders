1.	WHAT HOURS OF THE DAY HAD THE HIGHEST ORDER COUNT?

In the query I selected the relevant columns i.e. order id and order count. Using the COUNT function, I established the order count. Subsequently, I grouped the results based on order time and sorted them in descending order according to order count. Finally, I applied the LIMIT function to retrieve only the top 10 orders

2.	WHAT IS THE AVERAGE CUSTOMER RATING OF FOOD AND WHICH RESTAURANTS ARE ABOVE AND BELOW AVERAGE?

The query utilized the LEFT JOIN function to connect the orders and restaurants tables using the restaurant id key. I then filtered the results using the where statement to only indicate ratings at 5. Initially the query returned 88 so I applied the LIMIT function to narrow down the output to 20.

3.	WHICH ZONES REGISTERED THE HIGHEST ORDERS AND HOW DOES IT RELATE TO CATEGORY?

Since the query required information from 2 separate tables, I applied the LEFT JOIN function to connect them both using the restaurant id key. In the 	SELECT statement I input the relevant columns of zone, category and aggregated the COUNT of orders. Further to that, I grouped the results by zone and category then I finished it off by arranging the order count output in descending order.

4.	WHICH CUSTOMERS MADE THE MOST ORDERS AND WHAT PAYMENT MODE WAS USED?

In the SELECT statement of the query, I input the following columns, customer name, payment mode and order count using the COUNT function. Lastly I grouped the results by customer name and payment mode then ordered the output in descending order. To narrow down the output I applied a LIMIT of 10.

5.	WHAT IS THE CORRELATION BETWEEN DELIVERY TIME TAKEN AND DELIVERY RATING?

In the SELECT statement of this simplified query, I included the relevant columns i.e. delivery time taken and customer rating delivery. To effectively assess any potential correlation between delivery time and customer rating, I set a LIMIT of 30 to generate a substantial output range for comparison purposes.

To validate my finding I calculated the correlation coefficient using the CORR function. This gave me a result of - 0.05144020750543335


6.	WHAT IS THE STANDARD DEVIATION OF ORDERS PER RESTAURANT?

I structured a subquery within the FROM clause, wherein I included the order amount and restaurant name in the SELECT statement. Subsequently, I employed a LEFT JOIN to link the orders and restaurants tables via the restaurant ID key. Following this, I grouped the outcomes of the initial query by restaurant name. Subsequently, I formulated a secondary query where I selected the restaurant name in the SELECT statement. Utilizing the AVG function, I computed the average order amount, and by employing the STDDEV function, I determined the standard deviation. By transforming the inner query into a new table, the query was capable of comparing restaurant names with their respective means and standard deviations.


