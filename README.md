# Bangalore Real Estate Analytics Dashboard

An interactive Streamlit dashboard to analyze **Bangalore residential price trends (2015–2025)**, compare key micro-markets, and identify areas with attractive **risk–return** profiles for long-term investment decisions.

---

## 🌟 Project Overview

This project explores decade-long price evolution across major Bangalore micro-markets using:

- Historical average price per sqft by area and year  
- CAGR (long-term growth) as a proxy for returns  
- Year-on-year (YoY) growth and volatility as proxies for risk  
- A risk–return matrix to help decide **where to invest in the next 10 years**

The dashboard is built with **Streamlit**, **Pandas**, and **Matplotlib**.

---

## 📊 Key Features

- **Interactive filters**
  - Filter by micro-market / area  
  - Select custom year range (e.g., 2015–2025)

- **KPI cards**
  - Latest year average price (₹/sqft)  
  - Average growth over the selected period  
  - Number of areas analyzed  

- **Visualizations**
  - Price trend line chart by area  
  - Long-term **CAGR %** comparison by area  
  - **Volatility** (standard deviation of YoY % change) by area  
  - **Risk–return scatter plot** (CAGR vs volatility) to spot attractive zones for long-term investment

---

## 🗂️ Dataset

The app expects a CSV with columns like:

- `area` – micro-market name (e.g., Whitefield, Devanahalli)  
- `date` – observation date (parsed as datetime)  
- `year` – year (e.g., 2015–2025)  
- `avg_price_per_sqft` – average price per square foot (INR)  
- `yoy_pct` – optional; YoY % change in price (the app can compute this if missing)

Default path used in `app.py` (Colab-style):

```python
/content/sample_data/real_estate_bangalore_area_prices.csv
