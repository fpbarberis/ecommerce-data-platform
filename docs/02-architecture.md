# 02 - Architecture

## Business Domain

The project simulates an e-commerce company.

The initial entities are:

- Customers
- Products
- Orders
- Order Items
- Payments

## Data Flow

The analytical platform follows a layered architecture:

RAW
  ↓
STAGING
  ↓
INTERMEDIATE
  ↓
MARTS

## RAW

The RAW layer contains data as received from the source systems.

Minimal transformations should be performed at this stage.

## STAGING

The STAGING layer standardizes source data.

Typical transformations include:

- Renaming columns
- Casting data types
- Basic cleaning
- Standardizing values

## INTERMEDIATE

The INTERMEDIATE layer contains reusable business transformations.

This layer may contain:

- Joins
- Aggregations
- Deduplication
- Business logic

## MARTS

The MARTS layer contains analytical models intended for
business users and downstream consumers.

The initial marts will include:

### Dimensions

- dim_customers
- dim_products
- dim_date

### Facts

- fct_orders
- fct_payments

## Initial Architecture

Source Data
    ↓
Snowflake RAW
    ↓
dbt STAGING
    ↓
dbt INTERMEDIATE
    ↓
dbt MARTS
    ↓
Analytics / BI