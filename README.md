# RFM-Analysis-Dive-Deeper-Insights-into-Your-Customers-through-RFM-Segmentation
In this article (Updated in October 2023), we'll take a look at RFM (recency, frequency, monetary value) analysis, which is based on the behavior of customer groups (or segments)
![image](https://github.com/Hagar-zakaria/RFM-Analysis-Dive-Deeper-Insights-into-Your-Customers-through-RFM-Segmentation/assets/93611934/76492c20-f4c0-4b0c-ac63-fcbe2c148470)
This method of analysis allows you to study the behavior of users and how they make payments. As a result, you’ll receive valuable insights for direct marketing.

# What is RFM analysis ?
Imagine you run a store, and you want to figure out who your best customers are. Instead of getting lost in a sea of data, RFM helps you categorize customers based on when they last shopped with you (that's the '**"Recency"**'), how often they shop (that's the **"Frequency"**), and how much they tend to spend when they do (and that's the **"Monetary"** part).

So, with RFM, you can give a little extra love to your top customers and maybe nudge those who haven't been around in a while. It's a neat way to make sense of your customer base!

# Understanding RFM: Recency, Frequency, and Monetary Value

Let's dive in what R-F-M stands for a bit deeper and with more context. 

**Recency**: It’s all about the ‘when’. How long has it been since a customer made a purchase from you? If someone just bought something yesterday, they're probably more engaged with your brand than someone who hasn't shopped in a year. It's like remembering who came to your last party and who didn't. The ones who showed up recently are probably your closer buddies.

**Frequency**: Now, let's talk about the 'how often'. Some folks might pop into your store (or online site) regularly, like those coffee addicts who need their daily fix. Others might just drop by occasionally. Knowing how often someone shops with you can give you a good idea about their loyalty and how integral you are to their routine.

**Monetary**: Lastly, it’s about the 'how much'. This tells you about the buying power or spending habits of your customers. Some might be big buyers, always going for the premium items, while others might be more on the budget-friendly side. By understanding how much they typically spend, you can tailor your offers or promotions to suit their pocket.

![image](https://github.com/Hagar-zakaria/RFM-Analysis-Dive-Deeper-Insights-into-Your-Customers-through-RFM-Segmentation/assets/93611934/0e62bb10-136a-459c-9a9d-f3001ca00e6e)

By combining these three aspects, RFM Analysis helps businesses categorize their customers into different segments. For instance,**" a customer who scores high on all three aspects is a golden one "** — they shop frequently, they’ve shopped recently, and they spend a good amount. These are the buyers you’d want to roll out the red carpet for!

On the flip side, if someone hasn't shopped in ages, only comes by once in a lifetime, and barely spends anything, they might need a bit more incentive or engagement to get them back on track and increase their score.

All in all, RFM Analysis is a brilliant way to personalize your marketing efforts. Instead of treating all customers the same, you can understand their habits and preferences better and tailor your approach to match. It’s like having a cheat sheet for building stronger, more meaningful relationships with your customers and growing sales!

# Why RFM Analysis Matters for Your Business

1. Understanding Customers Better:
- RFM Analysis provides insights into customer behavior by analyzing Recency, Frequency, and Monetary value.
- It helps businesses understand what customers truly want by examining their buying patterns.
2. Tailoring Marketing Efforts:
- RFM enables targeted marketing campaigns tailored to specific customer segments.
- Crafting personalized promotions increases engagement and drives sales effectively.
3. Money and Effort Allocation:
- RFM guides resource allocation by focusing efforts on high-value customers for better ROI.
- Rather than spreading resources thinly, it advises concentrating on valuable segments.
4. Predicting Future Buying Behavior:
- RFM's predictive nature forecasts future customer actions based on past behavior.
- Anticipating needs and preferences allows proactive strategy formation for marketing and sales.
5. Building Relationships:
- By catering to customer habits and preferences, RFM fosters deeper connections.
- Demonstrating care leads to customer loyalty and positive word-of-mouth.
6. Conclusion:
- RFM Analysis bridges the gap between businesses and customers, facilitating meaningful relationships.
- It's not just about numbers but understanding people, essential for becoming a beloved brand.


# Getting Started with RFM Analysis: Step-by-Step Guide
When it comes to data analytics tasks, it all starts from the Plan: you define the Business Goals, the Questions you supposed to be asking and the Metrics you need to measure. 

In our case - we already know all that information, we want to improve the revenue from existing list by segmenting the uses, so we can create more targeted campaigns. Out questions as well as the metrics are related to the whole R-F-M framework. 

For each of these metrics, we assign customers to one of three groups, which are assigned a number from 1 to 3.

**"Recency"**:

1 – long-standing customers.
2 – relatively recent customers.
3 – recent customers.

**"Frequency"**:

1 – purchases rarely (single orders).
2 – purchases infrequently.
3 – purchases often.

**"Monetary value"**:

1 – low value of purchases.
2 – average value of purchases.
3 – high value of purchases.

Customers are assigned RFM values by concatenating their numbers for Recency, Frequency, and Monetary value. For example, customer 111 made one order with a low monetary value a long time ago. Customer 333, on the other hand, often makes large-value orders and made a purchase recently. Customers with 3’s in every category are your best customers.


# Step 1: Collect the necessary data
You will need data on customer transactions (orders), including the date of the transaction, the customer ID, and the monetary value of the transaction (order amount). This data can typically be obtained from your CRM, ERP or database.

# Step 2: Prepare data for analysis
With purchasing behavior data collected, the next move is to prepare our data for RFM analysis, we need to make our raw data analysis ready.

Let us assume you have a table of customer transactions.

- In Column A you have the Customer Identification - like userid,
- Column B  - Date of Transaction,
- Column C - Order Value

  ![image](https://github.com/Hagar-zakaria/RFM-Analysis-Dive-Deeper-Insights-into-Your-Customers-through-RFM-Segmentation/assets/93611934/b92de677-073c-4c88-8ca5-484d715d9cd7)

**RFM Data preparation in Google Sheets & Excel**
To calculate the recency in Google Sheets or Microsoft Excel, first we need to find the lates transaction date for each of the customers. Let's create a new column and call it DaysSinceTransaction.

The formula would be =TODAY()-B2. Here, 'TODAY()' returns the current date, and 'B2' refers to the cell containing the date of the last transaction for a particular transaction. The result will be the number of days since the transaction.

![image](https://github.com/Hagar-zakaria/RFM-Analysis-Dive-Deeper-Insights-into-Your-Customers-through-RFM-Segmentation/assets/93611934/753584d2-640b-4b1f-a225-e5addfcabf9a)

We’ve successfully gathered all the transactions and their corresponding customer IDs. Plus, we've also determined the **number of days that have passed since each transaction.** 

Given that our database contains a list of multiple transactions for individual customers, it's important to select only the most recent transaction date for each customer when calculating Recency.

So how do you pinpoint the latest transaction date after establishing the number of days passed since each transaction? 

Let's select the **data range** , click **Insert** -> **Pivot Table**. 

Add **Customer ID** as **Rows**.

Add **DaysSinceTransaction** as a Value. And summarize by **MIN**.

![image](https://github.com/Hagar-zakaria/RFM-Analysis-Dive-Deeper-Insights-into-Your-Customers-through-RFM-Segmentation/assets/93611934/7cb38526-234d-4828-9c2b-a0145d4ba841)

This would help us achieve us a smaller dataset with a single, latest transaction date per customer.

When the aforementioned steps are done correctly, Google Sheets will then generate a new pivot array. This dataset solely consists of rows showcasing each unique customer ID in tandem with their most recent transaction dates.

Next, add the Customer ID summarized by COUNTA to Values now to save our time later. 

Let's also calculate the total value of all orders for each customer. To do this, add Order Value as a Value to get the total amount spent per customer, and in the Summarize by column, indicate SUM.​

That’s it for analysis preparation.

Now we need to copy this pivot table data to a new sheet to calculate RFM values, and rename the columns to Recency, Frequency and Moneraty.

![image](https://github.com/Hagar-zakaria/RFM-Analysis-Dive-Deeper-Insights-into-Your-Customers-through-RFM-Segmentation/assets/93611934/f890acef-1ca5-4263-8c6a-d5e6907bfd3a)

**RFM Data preparation with SQL**

In SQL, you'd typically utilize the **DATEDIFF** function to get the **DaysSinceTransaction**. 

Assuming your table of customer transactions contains a column named **'DateOfTransaction'**, the SQL query would be:

```SELECT DATEDIFF(day, DateOfTransaction, GETDATE()) as DaysSinceTransaction FROM CustomerTransactions;```

This query returns a list of customers together with the transactions and the number of days since their last transaction. 

You can utilize SQL to fine-tune your data. It allows you to pick the most recent date for each customer by grouping the transactions by customer ID and using the MIN function. This SQL function gives you the been the lowest value in the selected column, in this case, the least amount of days since last transaction. 

Your SQL command may look like this: 


```
SELECT customer_id, MIN(DaysSinceTransaction)
FROM CustomerTransactions
GROUP BY customer_id
```

after running this command, you'll have a list with each customer's most recent transaction identificator, which aligns perfectly with the recency aspect of RFM Analysis. 

Once you've gathered the necessary data, you can pivot or group the 'customer_id' by the respective order value with SQL, helping you calculate the monetary value and frequency components of RFM. Start by running a simple query for this. 

Here's a substance to illustrate:


```
SELECT customer_id, SUM(order_value) AS total_order_value, COUNT(*) AS no_of_transactions
FROM CustomerTransactions
GROUP BY customer_id
```

This SQL statement does two things. It first groups all orders that belong to each customer, represented by the 'customer_id'. Following that, it calculates the total order value and the number of orders for each customer.

The 'SUM(order_value)' expression calculates the total spent by each customer, thus representing the 'Monetary' part of RFM. 

By applying 'COUNT(*)', the query counts the number of rows for each customer, thus representing the 'Frequency' part of RFM.

# Step 3: Calculate recency
The Recency score represents how recently a customer made a purchase, with a higher score indicating a more recent purchase.

The first thing we need to do is calculate how long **33%** and **66%** of our customers have bought from us. This is easily done using the formula =PERCENTILE.INC ([range]; 0.33) and = PERCENTILE.INC ([range]; 0.66).

We now know that **33%** of customers bought our products less than **11.28** days ago, and **66%** bought less than **14.28** days ago.​

Accordingly we assign those customers who bought less than 11.28 days ago the highest value of 3.
Those who placed an order from **11.28** to **14.28** days ago are assigned a value of 2.
The rest, who bought more than **14.28** days ago, we assign a value of 1.
All this can be automatically calculated with the formula =IF(B2<11.28; 3; IF(B2 <14.28; 2, 1)).
