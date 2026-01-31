# End-to-End Supermarket Operations & SLA Analytics (Airtable)

## Project Overview
This project uses a supermarket transaction dataset to design an end-to-end order fulfillment and SLA monitoring system in Airtable.
The goal was to transform flat historical sales data into a scalable operational workflow that tracks order delivery performance, customer value, and service-level agreement (SLA) compliance using data modeling, automation, and dashboards.

## Data Source
The dataset was obtained from a publicly available supermarket sales dataset, representing historical point-of-sale transactions.
The data includes order details, product categories, payment information, customer attributes, and transaction dates.

## Data Modeling & System Design
The original flat dataset was restructured into a relational data model to support analytics, automation, and scalability.
* Core Tables
- Customers
- Orders
- Products
- Order Items (bridge table)

Relationships
- The Orders table is linked to the Customers table to enable customer-level analytics.
- The Orders table is linked to the Products table through an Order Items table, creating a proper many-to-many relationship.
- Supporting fields and rollups were created to ensure accurate aggregation across tables.

## Key Fields & Metrics
* Orders Table
- Days to Deliver – Calculates how long it took to deliver an order.
- Fulfillment Status – Tracks order progress (Pending, Packed, Shipped, Delivered, Failed).
- SLA Target (Days) – The promised delivery timeframe.
- SLA Met – Indicates whether the supermarket met the SLA.
- SLA Breach – Flags orders that missed the SLA.
