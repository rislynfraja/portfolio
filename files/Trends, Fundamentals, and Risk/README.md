# Trends, Fundamentals, and Risk: A SQL Stock Analysis
### Group Projects Completed for CSE 4701 - Principles of Databases

---

Three SQL projects exploring stock market data from different analytical angles — price trends, company fundamentals, and portfolio risk. Each part has its own database schema, data insertion script, and set of analysis queries across 10 real stocks.

---

## Project Overview

| Project | Focus | Key Metric |
|---|---|---|
| Stock Price Trends & Volatility Analysis | Daily stock prices over 3+ months | Moving averages, volatility |
| Fundamental Analysis Earnings and Ratios | Earnings and financial ratios over 1 year | P/E ratio, dividend yield, profit margin |
| Portfolio Optimization and Risk Assessment | Daily returns over 6 months | Cumulative returns, risk by volatility |

---

## Project Deliverables (for each part)

- **ERD** — Entity-Relationship Diagram showing table structure and relationships
- **Schema Script** — SQL to create all tables
- **Data Insertion Script** — populated with real data for 10 stocks
- **Analysis Queries** — SQL queries answering the key questions below
- **Presentation** — findings, trends, and recommendations

---

## Project 1 — Stock Price Trends & Volatility Analysis

**Database Tables:**
- `Stocks` — stock_id, symbol, company_name, sector, industry
- `Stock_Prices` — price_id, stock_id, date, open_price, close_price, high, low, volume
- `Moving_Average` *(calculated)* — stock_id, date, 5_day_avg, 20_day_avg
  
**Analysis Queries:**
- Most volatile stocks by percentage price change
- Stocks with the highest average trading volume
- Stocks that have crossed above or below their moving averages

---

## Project 2 — Fundamental Analysis: Earnings & Ratios

**Database Tables:**
- `Companies` — company_id, symbol, company_name, sector, industry
- `Financials` — report_id, company_id, year, revenue, net_income, eps, dividend, market_cap
- `Ratios` *(calculated)* — company_id, year, pe_ratio, dividend_yield, profit_margin
  
**Ratios Calculated:**
```
P/E Ratio      = Market Cap / Net Income
Dividend Yield = Dividend / Market Cap
Profit Margin  = Net Income / Revenue
```

**Analysis Queries:**
- Most profitable companies by net income and profit margin
- Best dividend-paying stocks by dividend yield
- Companies with the highest revenue growth year-over-year

---

## Project 3 — Portfolio Optimization & Risk Assessment

**Database Tables:**
- `Stocks` — stock_id, symbol, company_name, sector
- `Historical_Returns` — return_id, stock_id, date, daily_return, cumulative_return
- `Portfolio` — portfolio_id, stock_id, allocation_percentage
  
**Analysis Queries:**
- Portfolio returns under different stock weightings
- Best-performing sector over the 6-month period
- Lowest-risk stocks measured by return volatility

---

## How to Run

1. Open your SQL environment
2. Run the schema creation script to set up the tables
3. Run the data insertion script to populate with stock data
4. Run the analysis queries to reproduce the findings

---

