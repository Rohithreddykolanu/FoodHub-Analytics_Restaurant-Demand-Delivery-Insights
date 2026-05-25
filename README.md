<h1 align="center">FoodHub Analytics - Restaurant Demand & Delivery Insights</h1>

<p align="center">
  <img alt="Python" src="https://img.shields.io/badge/Python-3.10+-3776AB?logo=python&logoColor=white">
  <img alt="pandas" src="https://img.shields.io/badge/pandas-2.2-150458?logo=pandas&logoColor=white">
  <img alt="NumPy" src="https://img.shields.io/badge/NumPy-2.0-013243?logo=numpy&logoColor=white">
  <img alt="Matplotlib" src="https://img.shields.io/badge/Matplotlib-3.10-11557C">
  <img alt="seaborn" src="https://img.shields.io/badge/seaborn-0.13-4C72B0">
</p>

## Overview

FoodHub is a food-aggregator app that connects customers in New York with a wide range of restaurants and manages the end-to-end delivery process. This project performs an exploratory data analysis (EDA) of FoodHub's order data to understand restaurant demand, cuisine popularity, customer ratings, and delivery performance, and turns those findings into concrete business recommendations.

## Problem Statement

The data science team needs answers to a set of business questions that will help the company improve customer experience and grow the platform: Which restaurants and cuisines drive demand? How satisfied are customers? How efficient is delivery, and where are the bottlenecks? The analysis below addresses these questions and proposes data-backed actions.

## Dataset

The dataset contains **1,898 orders** across **9 columns**, with no missing values.

| Column | Description |
| --- | --- |
| `order_id` | Unique ID of the order |
| `customer_id` | ID of the customer who placed the order |
| `restaurant_name` | Name of the restaurant |
| `cuisine_type` | Cuisine ordered by the customer |
| `cost_of_the_order` | Cost of the order |
| `day_of_the_week` | Weekday (Mon–Fri) or Weekend (Sat–Sun) |
| `rating` | Customer rating out of 5 (some orders are unrated) |
| `food_preparation_time` | Minutes from order confirmation to pickup |
| `delivery_time` | Minutes from pickup to drop-off |

## Approach

1. **Data understanding:** shape, data types, and missing-value checks.
2. **Univariate analysis:** distributions of numeric and categorical fields using histograms, box plots, and count plots (including a custom `histogram_boxplot` helper that stacks a box plot over a histogram with mean/median markers).
3. **Bivariate & multivariate analysis:** relationships between cost, preparation time, delivery time, cuisine, rating, and day of week (correlation heatmap, grouped aggregates).
4. **Business questions:** demand concentration, cuisine popularity, rating behaviour, and delivery efficiency.
5. **Conclusions & recommendations:** translating insights into actions.

## Key Findings

- **Demand is concentrated** among a few strong brands; restaurants such as Shake Shack, The Meatball Shop, and Blue Ribbon Sushi lead in both order volume and revenue.
- **American cuisine is the most popular**, followed by Japanese and Italian, with demand peaking on weekends.
- **Ratings skew positive** (mostly 4–5 stars), but **736 orders are unrated**, limiting feedback.
- **Food preparation** averages **27.37 minutes** (range 20–35 minutes).
- **Delivery is faster on weekends** (≈22.5 min) than on weekdays (≈28.3 min).
- About **10.5% of orders take more than 60 minutes** end-to-end; roughly **89% are delivered within an hour**.
- **Cost, preparation time, and delivery time are weakly correlated**, suggesting stable operations regardless of order value.

## Recommendations

- Promote high-performing, highly rated restaurants through featured placement and targeted offers.
- Improve weekday delivery by optimizing staffing, routing, and restaurant–driver coordination.
- Investigate the causes behind orders exceeding 60 minutes to reduce delays.
- Encourage ratings via small incentives (coupons, loyalty points) to collect more feedback.
- Strengthen partnerships with popular cuisines (American, Japanese) while supporting lower-performing restaurants with promotions.
- Introduce loyalty programs to improve retention and repeat orders.

## Tech Stack

Python · pandas · NumPy · Matplotlib · seaborn · Jupyter
