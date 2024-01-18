# Getting Started

 Clone the repository: git clone https://github.com/Dania-Ahmed12/PowerBi-Dashboards.git
Follow the instructions in the Power BI section to set up and run the analysis.

## Power BI
Open the Power BI file: SuperSalesAnalysis.pbix
Connect to your dataset and follow the steps outlined in the README.md file

# Super Sales Analysis with Power BI

## Overview

Welcome to the Super Sales Analysis repository! This project focuses on analyzing sales and profit data using Power BI. It provides insights into specific months, shipping modes, subcategories, and categories. Additionally, sales forecasting has been implemented using time series data.

## Table of Contents

- [Analyzing Sales and Profit](#analyzing-sales-and-profit)
  - [Identify Months with Lower Sales but Higher Profit](#1-identify-months-with-lower-sales-but-higher-profit)
  - [Determine Preferred Shipping Mode](#2-determine-preferred-shipping-mode)
  - [Analyze Subcategories and Categories](#3-analyze-subcategories-and-categories)
- [Key Performance Indicators (KPIs)](#key-performance-indicators-kpis)
- [Sales Forecasting](#sales-forecasting)
  - [Tips for Sales Forecasting](#tips-for-sales-forecasting)
  - [Example DAX Measures](#example-dax-measures)

## Analyzing Sales and Profit

### 1. Identify Months with Lower Sales but Higher Profit

- Create visuals for both sales and profit by month.
- Analyze and compare sales and profit for these months.

### 2. Determine Preferred Shipping Mode

- Create a visual representation of sales by shipping mode.
- Identify and highlight the shipping mode with the highest sales, likely "Standard Delivery."

### 3. Analyze Subcategories and Categories

- Create visuals for sales and profit by subcategory.
- Identify the top 3 subcategories (e.g., Chair, Binder, Phone).
- Create visuals for sales and profit by category (Office Supplies, Furniture, Technology).

## Key Performance Indicators (KPIs)

- Define KPIs relevant to your analysis. Examples:
  - Monthly Sales Growth Rate
  - Profit Margin
  - Average Order Value
  - On-Time Delivery Rate

## Sales Forecasting

- Utilize time series data based on order dates for forecasting.
- Use Power BI's forecasting capabilities or implement time series forecasting algorithms using DAX.

## Tips for Sales Forecasting

- Use the "Order Date" as your time series data.
- Consider using DAX functions like  AVERAGEX, to create measures for forecasting.
- Incorporate historical data patterns and seasonality for more accurate forecasts.

## Example DAX Measures

```DAX
# Sales Forecast Measure

SalesForecast = 
SUMMARIZE(
    'SuperStore Sales DataSet converted',
    'SuperStore Sales DataSet converted'[Order Date],
    "totalSales",
    SUM('SuperStore Sales DataSet converted'[Sales])
)

