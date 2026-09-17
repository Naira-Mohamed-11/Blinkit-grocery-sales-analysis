# 🛒 Blinkit Grocery Sales & Operations Analysis

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Naira-Mohamed-11/Blinkit-grocery-sales-analysis/blob/main/Blinkit_Grocery_Sales_Analysis.ipynb)

<div align="center">
  <img src="https://media.fashionnetwork.com/m/7882/4ac1/77da/8a18/45bb/1fbc/2c6a/b10f/14e5/863c/863c.png" width="700" alt="Blinkit Banner"/>
</div>

---

## Executive Summary

This project performs an end-to-end exploratory data analysis (EDA) on transaction, customer, logistics, and inventory data from **Blinkit** (an Indian quick-commerce grocery delivery service). 

The primary objective is to evaluate operational performance, understand buyer behavior across customer segments, track sales revenue trends, optimize inventory levels, and identify operational bottlenecks in delivery fulfillment.

---

## Key Objectives & Focus Areas

* **Sales & Revenue Optimization:** Track overall revenue, analyze average order value (AOV), and evaluate pricing sensitivity across product categories.
* **Customer Segmentation & Behavior:** Categorize customers (`Premium`, `Regular`, `New`, `Inactive`), analyze retention, and examine purchasing patterns.
* **Logistics & Delivery Performance:** Monitor delivery efficiency, compare promised vs. actual delivery times, and analyze order delay factors.
* **Inventory & Stock Management:** Assess product shelf-life, stock turnover, and identify risk areas for stockouts or product expiration.
* **Marketing & Customer Feedback:** Measure marketing campaign effectiveness and customer satisfaction scores.

---

## Dataset Overview

The analysis integrates multiple interconnected datasets:

| Dataset Name | Key Attributes | Description |
| :--- | :--- | :--- |
| **`customers`** | `customer_id`, `customer_segment`, `avg_order_value`, `area` | Customer demographics, order history, and behavior segments. |
| **`orders`** | `order_id`, `order_date`, `delivery_status`, `payment_method` | Core order metadata including timestamp logs and payment modes. |
| **`order_items`** | `order_id`, `product_id`, `quantity`, `unit_price` | Item-level transactional records. |
| **`products`** | `product_id`, `category`, `mrp`, `shelf_life_days`, `margin_percentage` | Product catalog details, pricing structures, and inventory thresholds. |
| **`delivery_performance`**| `delivery_partner_id`, `distance_km`, `delay_reasons` | Delivery logistics, fulfillment speeds, and transit metrics. |
| **`inventory`** | `store_id`, `stock_level`, `expiration_date` | Store-level stock metrics and product turnover rates. |
| **`customer_feedback`**| `rating`, `feedback_text`, `category` | Customer reviews and satisfaction ratings. |

---

## Data Preprocessing & Pipeline

1. **Data Ingestion & Cleaning:**
   * Parsed date strings into proper `datetime64` representations (`registration_date`, `order_date`, `promised_delivery_time`, `actual_delivery_time`).
   * Converted categorical variables (`customer_segment`, `delivery_status`, `payment_method`) to optimized `category` data types for computational efficiency.
2. **Feature Engineering:**
   * Calculated fulfillment variance (Actual vs. Promised delivery times).
   * Aggregated customer-level lifetime value and purchasing frequency metrics.
3. **Exploratory Data Analysis (EDA):**
   * Implemented statistical visualizations using `Seaborn` and `Matplotlib` to extract actionable business insights.

---

## Tech Stack & Tools

* **Programming Language:** Python 3.x
* **Data Manipulation:** `pandas`, `numpy`
* **Data Visualization:** `seaborn`, `matplotlib`
* **Environment:** Google Colab / Jupyter Notebooks
* **Version Control:** Git & GitHub

---

## How to Run locally

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/Naira-Mohamed-11/Blinkit-grocery-sales-analysis.git](https://github.com/Naira-Mohamed-11/Blinkit-grocery-sales-analysis.git)
   cd Blinkit-grocery-sales-analysis
