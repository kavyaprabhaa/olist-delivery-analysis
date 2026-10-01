# Do Late Deliveries Hurt Customer Satisfaction? (Olist E-Commerce)

## Business question
How much do late deliveries affect customer reviews and repeat purchases, and where should the company fix delivery first?

## Dataset
Brazilian E-Commerce Public Dataset by Olist (Kaggle). I used the orders, customers, order items, and reviews tables. After keeping delivered orders with a review, 95,824 orders remained.

## Tools
- Python (pandas, matplotlib) in Google Colab: cleaning, analysis, charts
- SQL (SQLite): validated results with GROUP BY, aggregations, and a JOIN
- Tableau Public: dashboard

## Method
1. Kept delivered orders and removed orders with no delivery date.
2. Created delivery days, delay days (delivered date minus estimated date), and a late flag.
3. Joined review scores to orders.
4. Compared ratings, repeat purchase rates, and late rates by state and city.

## Key findings
- 6.7% of orders arrived after the estimated delivery date.
- Late orders averaged 2.27 stars vs 4.29 for on-time orders.
- Ratings fall as delays grow: 4.29 (on time), 3.29 (1-3 days late), 2.11 (4-7 days late), 1.70 (7+ days late).
- Customers whose first order was late returned less often (2.56% vs 3.01%). Repeat purchases are rare overall and the effect is small, so this shows a pattern, not proof of cause.
- Late deliveries concentrate in the northeast: Alagoas 20.8%, Maranhao 17.1%, Sergipe 15.0%. The city of Maceio had a 26.5% late rate.
- About 7.3% of revenue (953K of 13.1M BRL) came from late orders.

## Recommendations
1. Prioritize delivery improvements in AL, MA, and SE, starting with cities like Maceio, Teresina, and Sao Luis.
2. Add buffer days to delivery estimates in high-delay regions.
3. Proactively message customers when an order is running late.

## Limitations
- Only orders with reviews were analyzed.
- The estimate of lost repeat revenue is small and rests on a simple assumption (late-order customers returning at the on-time rate).

## Dashboard
!(dashboard.png)
Live dashboard:https://public.tableau.com/app/profile/kavya.j8348/viz/OlistDeliveryDelayAnalysis/Dashboard1?publish=yes

## Files
- `OLIST ANALYSIS.ipynb`: full analysis in Python and SQL
