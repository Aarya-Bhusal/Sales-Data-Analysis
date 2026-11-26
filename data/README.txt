# Sales Analytics Dataset (Synthetic)

This is a synthetic retail dataset generated for data-analysis practice. It is not real customer or business data.

## Tables
- transactions.csv: 600,000 transaction line items from 2023–2025.
- customers.csv: 50,000 customer profiles.
- products.csv: 2,000 products with category, cost, price, and supplier.
- stores.csv: 60 stores / fulfillment locations.
- returns.csv: return records for transactions marked returned.

## Join keys
- transactions.customer_id -> customers.customer_id
- transactions.product_id -> products.product_id
- transactions.store_id -> stores.store_id
- returns.transaction_id -> transactions.transaction_id

## Suggested metrics
- Revenue: sum of net_sales (be careful with returns/refunds and returned flags)
- Gross sales: sum of gross_sales
- Estimated profit: sum of estimated_profit (not adjusted for refunds/return processing costs)
- Average order/transaction value: net_sales per transaction row (this dataset is line-item based, so transaction_id is a unique row)
- Return rate: returned rows / rows
- Discount rate: weighted discount or average discount_pct; explain which you use

## Notes
Data intentionally includes patterns and randomness. Treat it as exploratory, not a source of real-world conclusions.
