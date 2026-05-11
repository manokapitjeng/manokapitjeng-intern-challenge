# ShopRite Analytics Findings

## Summary

I cleaned and analysed 12 months of retail sales data for ShopRite Analytics. The dataset included sales from physical stores and the online channel.

Before analysis, the data needed cleaning because it had inconsistent store names, province names, product categories, mixed date formats, missing values, negative return transactions, and possible duplicate records.

After cleaning the dataset, I answered the five business questions from the prompt, created simple visualisations, predicted next month’s revenue per store, and added a bonus customer insight.

The main finding is that revenue increases strongly towards the end of the year, especially around November and December. Online is an important sales channel, Electronics is the best-performing product category, and Limpopo has the highest average revenue per transaction.

---

## Part 1: Data Cleaning

The dataset had several issues that needed to be cleaned before doing analysis.

Some column names were not immediately clear, so I renamed them to easier English names:

- datum became transaction_date
- kategorie became category
- bedrag became revenue

I cleaned store names because some malls appeared in different formats. For example, some stores had slightly different names, spelling, or capitalisation. I standardised these names so the same store would not be counted separately.

I also cleaned province names and category names because the same issue appeared there. This was important because the analysis uses groupby(), and inconsistent names would split the same store, province, or category into different groups.

Missing store values were treated as Online because online transactions may not have a physical store linked to them.

The revenue column needed cleaning because some values had currency symbols, spaces, commas, brackets, or negative values. I converted the revenue column into a numeric format so that I could calculate totals, averages, trends, and forecasts.

The date column had mixed formats, so I converted it into a proper date format and created a `month` column for monthly analysis.

I also checked duplicate rows and duplicate transaction IDs. I did not automatically delete similar-looking rows because in retail data, different customers can make similar purchases on the same day.

Negative revenue values were treated as returns, not errors. I separated returns from normal sales so that the sales analysis could focus on actual sales revenue while still keeping returns as useful business records.

---

## Part 2: Business Questions

### 1. Top 5 stores by total revenue

The top 5 stores/channels were:

1. Online
2. Menlyn Park
3. Canal Walk
4. Eastgate
5. Baywest Mall

Online generated the highest total revenue as an individual channel. This shows that the online channel is important to the business and should not be treated as a small side channel.

Among the physical stores, Menlyn Park, Canal Walk, Eastgate, and Baywest Mall were strong performers. These stores should be prioritised for stock availability, staffing, and promotions because they contribute strongly to revenue.

---

### 2. Best-performing product category and growth trend

The best-performing product category was **Electronics**.

Electronics showed strong growth across the year, especially towards the end of the year. This suggests that Electronics is a major revenue driver for the business.

The strong year-end performance may be linked to peak shopping periods such as Black Friday and the holiday season.

From a business point of view, ShopRite Analytics should make sure Electronics stock levels are planned properly before November and December. Poor stock availability during this period could lead to missed revenue opportunities.

---

### 3. Seasonal sales pattern

There was a clear seasonal pattern in the data.

Revenue was weaker earlier in the year and increased strongly towards the end of the year. November and December stood out as strong sales months.

This suggests that the business benefits from year-end shopping behaviour, promotions, and holiday-season demand.

The business should prepare early for this period by planning stock, staffing, delivery capacity, and marketing campaigns before the peak months.

---

### 4. Province with highest average transaction value

**Limpopo** had the highest average transaction value.

This means that customers linked to Limpopo spent more per transaction on average than customers in other provinces.

Limpopo may not necessarily have the highest total revenue, but the average transaction value shows that purchases linked to this province were higher in value.

The business could investigate which products are driving this higher average spend and whether similar strategies can be used in other provinces.

---

### 5. Online vs in-store sales trend

I compared online and in-store revenue over time.

Both online and in-store revenue showed growth across the year. In-store revenue remains important because it includes multiple physical stores, but online revenue is also strong as a separate channel.

This shows that the business should continue supporting both channels.

For physical stores, the business should focus on stock, customer service, and store operations. For online, the business should focus on website experience, reliable fulfilment, delivery, and digital promotions.

The online channel should continue to be monitored because it may become an even bigger part of total revenue over time.

---

## Part 3: Prediction

For the prediction section, I predicted next month’s revenue per store.

I used a simple baseline method: **average monthly revenue per store**.

I first grouped the data by store and month to calculate monthly revenue for each store. Then I calculated the average monthly revenue for each store and used that as the prediction for next month. However, it gives a useful starting point because it is based on each store’s past monthly performance.

With more time, I would improve the forecast by adding seasonality, previous month revenue, rolling averages, promotions, and more historical data.

---

## Part 4: 

For the bonus insight, I investigated customer behaviour.

I grouped the sales data by customer ID and looked at:

- total revenue
- number of transactions
- number of stores used
- monthly spending trend

The top customer was **CUST-00042**.

This customer had high total revenue, multiple transactions, and purchases across different stores. This stood out because it may show that the customer is a valuable repeat customer or a possible bulk buyer.

This kind of customer insight can help the business identify valuable customers for retention, loyalty campaigns, targeted offers, or account management.

However, because the customer appears across different stores and has high-value activity, the business could also review the transactions to confirm that the activity is legitimate and not a data quality issue.

---

## Recommendation

The business should focus on four main areas:

1. **Support the online channel**

Online is a strong individual revenue channel. The business should continue improving online shopping, delivery, fulfilment, and digital promotions.

2. **Prepare earlier for November and December**

Revenue increases strongly towards the end of the year. The business should prepare stock, staffing, marketing, and delivery capacity before the peak period.

3. **Prioritise Electronics**

Electronics is the best-performing category and shows strong year-end performance. This category should be planned carefully before peak sales months.

4. **Pay attention to high-value customers**

Customers such as CUST-00042 may be important for loyalty, retention, or targeted offers. The business should investigate high-value customers further.

---

## Final Finding

The cleaned dataset helped answer the main business questions from the prompt.

The analysis showed performance by store, category, province, month, channel, and customer.

The forecast was kept simple and beginner-friendly, but it still gave a basic estimate of next month’s revenue per store.

The bonus customer insight added another useful business view by showing which customer contributed strongly to revenue and how their spending changed over time.
