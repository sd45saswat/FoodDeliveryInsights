# 🍽️ Food Delivery Data Analytics Project

A complete **end-to-end data analytics project** that integrates data from **CSV, JSON, and MySQL**, performs **business-driven analysis**, and creates **professional visualizations** using Python.

This project is designed to be **portfolio-ready, interview-ready, and hackathon-ready**.

---

## 📌 Project Overview

This project analyzes a food delivery platform to uncover insights related to:
- User behavior (Gold vs Non-Gold members)
- Revenue trends
- Restaurant performance
- Cuisine preferences
- City-wise and time-based analytics

The workflow covers **data ingestion → merging → analysis → visualization → insights**.

---

## 🧱 Data Sources

| Dataset | Format | Description |
|-------|--------|-------------|
| `orders.csv` | CSV | Order-level transaction details |
| `users.json` | JSON | User information & membership status |
| `restaurants` | MySQL Table | Restaurant name, cuisine & ratings |

---

## 🔗 Data Integration

### Joins Performed
- **Orders ↔ Users**
  - Join Type: `LEFT JOIN`
  - Key: `user_id`
- **Orders ↔ Restaurants**
  - Join Type: `LEFT JOIN`
  - Key: `restaurant_id`

> Left joins ensure **all orders are retained**, even if user or restaurant data is missing.

---

## 🛠️ Tech Stack

- **Python 3**
- **Pandas** – Data manipulation & analysis
- **MySQL** – Restaurant database
- **Matplotlib** – Core visualizations
- **Seaborn** – Advanced statistical plots
- **Jupyter Notebook**

---

## ⚙️ Data Pipeline

```text
orders.csv  ─┐
             ├──► Pandas Merge ───► final_food_delivery_dataset.csv
users.json  ─┘
                  ▲
                  │
            MySQL (restaurants)
