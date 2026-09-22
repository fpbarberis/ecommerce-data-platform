# ecommerce-data-platform 

# 01 - Project Overview

## Why are we building this project?

This project is designed to learn Snowflake and dbt through
a realistic Data Engineering use case.

The objective is not to reproduce a tutorial, but to build
a small production-like analytical data platform.

## Business Scenario

We are working with an e-commerce company that generates
data from customers, products, orders and payments.

The company wants to analyze:

- Revenue
- Orders
- Customers
- Product performance
- Customer behavior

## Main Engineering Problem

Raw operational data is not directly suitable for analytics.

We need to:

1. Ingest the data
2. Store the raw data
3. Clean and standardize it
4. Transform it into analytical models
5. Validate data quality
6. Make the models available for analytics

## Technologies

### Python

Used for ingestion and data processing where appropriate.

### Snowflake

Used as the analytical data warehouse.

### dbt

Used to transform, test and document data inside Snowflake.

### Git

Used for version control and collaboration.