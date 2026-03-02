# 🪑 Furniture Manufacturing ERP Database

A comprehensive, normalized (3NF) relational database system designed to manage the end-to-end operations of a furniture manufacturing and retail company. 

## 🎯 Overview
This project models the complex business logic of a manufacturing facility, handling everything from raw material inventory and supplier management to production capacity planning and customer order fulfillment. It ensures strict data integrity through advanced SQL constraints and relationships.

## 🛠️ Tech Stack
* **Database:** MS SQL Server / T-SQL
* **Concepts:** Relational Schema Design, 3NF Normalization, Computational Columns, Data Integrity Constraints.

## ⚙️ Key Features & Schema Highlights
* **Production Planning:** Calculates required man-hours and machine-hours against the actual `WorkCalendar` capacity.
* **Inventory Management:** Tracks both finished `Products` and raw `Parts` linked to specific `Suppliers`.
* **Order Processing:** Manages customer orders with strict chronological constraints (Order -> Ship -> Delivery dates) and discount logic.
* **Data Integrity:** Implements over 20 rigorous `CHECK` constraints to prevent logical errors (e.g., negative stock, invalid postal codes, incorrect VAT/Margin ranges).

## 📄 Database Schema Architecture
The database encompasses several interconnected domains:
1.  **Products & Construction:** `Products`, `Parts`, `ProductConstruction`
2.  **Operations:** `ProductionPlan`, `WorkCalendar`
3.  **Sales:** `Orders`, `OrderDetails`, `Customers`
4.  **Supply Chain:** `Suppliers`
5.  **Finance:** `CostParameters` (tracks historical labor, utility rates, and margins).
