# From Click to Glow: Marketing Efficiency, Customer Journey & Product Performance Dashboard

An interactive Power BI dashboard for a Direct-to-Consumer (D2C) beauty and skincare brand. It tells one story, from ad click to product sold, so non-technical decision-makers can see which channels are efficient, where customers drop off, and which products actually perform.

> Team: Aku UNS | Participant ID: VISBI26034
> Built by Arif Nuri Setiawan, Ilham Ghozali

## Business Problem
Beauty D2C brands run many channels at once (Meta Ads, Google Ads, TikTok Ads, KOL, email, marketplaces), so data is scattered across sources. This dashboard consolidates it to answer three questions:
1. Which marketing channels are truly efficient?
2. At which funnel stage do potential buyers drop off?
3. Which products are actually the most profitable, not just the most talked about?

## Dashboard Pages
| Page | Focus |
|------|-------|
| Welcome | Landing page and navigation |
| Overview ("The Full Picture") | Total spend, revenue, ROAS, funnel conversion, monthly trend, revenue by channel |
| Marketing Efficiency ("Where the Money Works") | Budget variance, CPA, CTR, CVR Ads, ROAS vs CPA by channel and campaign |
| Customer Journey ("Who Makes It to Checkout") | Funnel stages, drop-off analysis, device and user-type breakdown |
| Product Performance ("What Sells, What Stalls") | Revenue, margin, rating, and refund rate by product and category |

## Key Insights
- **The ROAS gap:** Meta Ads has the largest spend but is the least efficient channel, while Email Marketing and WhatsApp Broadcast deliver much higher ROAS on small budgets (best email campaign: 34.6x ROAS).
- **The checkout cliff:** Overall funnel conversion is only ~5%, and the biggest drop-off is from Add to Cart to Checkout. Mobile converts better than desktop (6.6% vs 4.5%).
- **Rating isn't revenue:** Bundle is the top revenue category, and the highest-rated product is not the best seller.

## Data Preprocessing
Cleaning was done in Power Query in seven prioritized steps:
1. Standardized key columns and data types
2. Fixed numeric columns stored as text
3. Validated foreign-key integrity across tables
4. Resolved duplicate primary keys (14 duplicate order IDs)
5. Standardized categorical values (order status, refund status, gender)
6. Investigated numeric anomalies (negative values, clicks > impressions)
7. Handled missing values based on business context

All assumptions and decisions are documented in the project report.

## Data Model
Star schema with four fact tables (`fact_marketing_daily`, `fact_orders`, `fact_web_events`, `fact_budget`) and six dimensions (`dim_channel`, `dim_campaign`, `dim_product`, `dim_customer`, `dim_kol`, `dim_date`).

## Key DAX Measures
`Total Spend` · `ROAS` · `CPA` · `CTR` · `CVR Ads` · `Funnel Conversion Rate` · `Refund Rate` · `Budget Variance %`

## Business Recommendations
- Reallocate part of the Meta Ads budget to Email Marketing and WhatsApp Broadcast to lift blended ROAS.
- Improve the checkout experience, especially on desktop, to reduce drop-off.
- Expand the Bundle product line while using high-rated products to build brand credibility.

## Tools
Power BI Desktop · Power Query · DAX

## How to Open
Download `dashboard_visbi.pbix` and open it with Power BI Desktop.

