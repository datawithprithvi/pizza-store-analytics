# 🍕 Pizza Store Analytics

An end-to-end data analytics project that turns raw pizza store sales data into an interactive, live dashboard — built with SQL, Python, and Streamlit.

**🔗 Live Dashboard:** https://pizza-store-analytics-obtvo2ut6ifkc6ofudzqv4.streamlit.app

## Overview

This project analyzes order-level sales data from a pizza store to uncover patterns in customer ordering behavior, product mix, and daily revenue. Data was originally stored across multiple relational tables in MySQL, joined and cleaned in Python, then visualized through an interactive dashboard.

## Key Insights

- **439** unique orders analyzed, generating a full sales dataset of 1,000 order-line records
- Average order value: **~$59**
- Customers order an average of **3 unique pizzas** per order
- **Small** pizzas are the most ordered size, far ahead of Medium, Large, and XL
- Order volume peaks around **12 PM and 6 PM** — a classic lunch/dinner rush pattern
- **Classic** is the top-performing pizza category by order count

## Tools & Tech Stack

- **MySQL** — relational data storage, multi-table joins
- **Python (Pandas, NumPy)** — data cleaning, feature engineering, aggregation
- **Plotly** — interactive visualizations
- **Streamlit** — dashboard deployment

## Project Workflow

1. **Data extraction** — joined 4 normalized MySQL tables (orders, pizzas, sales, order details) into a single dataset using `pymysql`
2. **Data cleaning** — resolved duplicate columns from the multi-table join, converted data types, engineered a proper datetime field from separate date/time columns
3. **Analysis** — calculated KPIs (total orders, average order value, size/category performance, hourly and daily trends)
4. **Dashboard** — built an interactive Streamlit app with filters for pizza category and size, live KPI cards, and charts

## Files in This Repo

| File | Description |
|---|---|
| `The Pizza Store.ipynb` | Full analysis notebook — data cleaning, exploration, and insights |
| `pizza_app.py` | Streamlit dashboard app |
| `pizza_data.csv` | Cleaned dataset powering the dashboard |
| `requirements.txt` | Python dependencies |

## Run It Locally

```bash
git clone https://github.com/datawithprithvi/pizza-store-analytics.git
cd pizza-store-analytics
pip install -r requirements.txt
streamlit run pizza_app.py
```
