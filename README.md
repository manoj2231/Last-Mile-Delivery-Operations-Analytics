# Last-Mile Delivery Operations Analytics

A MySQL business analytics project exploring delivery demand, customer behavior, delivery performance, and resource utilization for a QuickRoute logistics company.

## Project Overview

QuickRoute Logistics is a last-mile delivery company serving customers across multiple delivery zones. This project uses MySQL and SQL to analyze its operational data and identify patterns, performance gaps, and opportunities for improvement.

The analysis focuses on transforming relational data into meaningful business insights that can support operational decision-making.

## Business Objectives

- Understand delivery demand across zones, service types, priorities, and time periods.
- Analyze customer ordering behavior and order value.
- Evaluate delivery outcomes, durations, and performance trends.
- Assess driver workload and vehicle utilization.
- Identify failed, pending, rescheduled, and repeated delivery attempts.

## Tools & Technologies

- MySQL
- SQL
- MySQL Workbench
- Microsoft PowerPoint
- GitHub

## Dataset Overview

The database contains five relational tables and 7,030 records.

| Table      | Records | Description                                          |
| ---------- | ------: | ---------------------------------------------------- |
| Customers  |     400 | Customer profiles and delivery zones                 |
| Orders     |   3,000 | Order details, service types, priorities, and values |
| Deliveries |   3,500 | Delivery status, attempts, distance, and duration    |
| Drivers    |      80 | Driver details, ratings, and availability            |
| Vehicles   |      50 | Vehicle types, fuel types, and capacity              |

## Database Relationships

- Customers → Orders: One customer can place multiple orders.
- Orders → Deliveries: One order can have multiple delivery records.
- Drivers → Deliveries: Each delivery record references a driver.
- Vehicles → Deliveries: Each delivery record references a vehicle.

## Analysis & Key Findings

### 1. Delivery Demand

- 3,000 orders generated a total order value of 7.52 million.
- ZONE0005 recorded the highest order volume with 240 orders.
- Standard was the most popular service type with 620 orders.
- December recorded the highest monthly order volume with 293 orders.

### 2. Customer Behavior

- Individual customers accounted for 68.3% of orders.
- Business customers had a higher average order value.
- 397 out of 400 customers placed multiple orders.

### 3. Delivery Performance

- 2,581 of 3,500 delivery records were marked Delivered (73.7%).
- 295 delivery records were marked Failed.
- Express had the highest delivered share at 76.9%.

### 4. Driver & Vehicle Performance

- 75 of 80 drivers were active.
- All 50 vehicles were marked active.
- The average driver rating was 3.05 out of 5.

### 5. Delivery Problems

- 919 delivery records were not marked Delivered.
- 925 orders had no matching delivery record.
- Some orders had up to six delivery records.

## Business Recommendations

- Allocate drivers and vehicles according to demand across zones.
- Investigate zones and service types with higher failure rates.
- Confirm customer availability before delivery to reduce repeat attempts.
- Monitor driver performance and provide targeted coaching.
- Improve order-to-delivery record completeness.

## Repository Structure

```text
├── data/
├── sql/
│   └── SQL_project.sql
├── documentation/
│   ├── Project_Documentation.docx
│   └── Project_Presentation.pptx
├── screenshots/
├── README.md
├── LICENSE
└── .gitignore
```

## How to Use

1. Download or clone this repository.
2. Open MySQL Workbench.
3. Create or select a MySQL database.
4. Import the provided CSV files into the corresponding tables.
5. Open `sql/SQL_project.sql` and execute the queries to explore the analysis.

## Disclaimer

This project uses a dataset provided for educational and analytical purposes.
