# Pharmacy-Sales-System-
Pharmacy Sales System  This project is a simple **Pharmacy Sales Database** for managing **drug sales**, customers, and inventory. It is built using **MySQL** and includes SQL scripts for creating tables, inserting data, querying sales, and automatically updating stock after each sale using triggers.
## Project Structure

- `sql/create_database.sql` - Creates the database and tables (`Drugs`, `Customers`, `Sales`).
- `sql/insert_data.sql` - Inserts sample data for drugs, customers, and sales.
- `sql/queries.sql` - Contains example queries for:
  - Displaying all drugs and customers
  - Viewing sales details
  - Calculating revenue by drug or customer
  - Searching drugs by name
  - Reporting sales by date
- `sql/triggers.sql` - Trigger for **automatic stock update** after each sale.

## Tables

### Drugs
| Column            | Type          | Description                  |
|------------------|---------------|------------------------------|
| DrugID           | INT PK        | Unique ID for each drug       |
| Name             | VARCHAR(100)  | Drug name                     |
| Manufacturer     | VARCHAR(100)  | Drug manufacturer             |
| Price            | DECIMAL(10,2) | Price per unit                |
| StockQuantity    | INT           | Current stock in inventory    |

### Customers
| Column           | Type          | Description                  |
|-----------------|---------------|------------------------------|
| CustomerID      | INT PK        | Unique ID for each customer  |
| FirstName       | VARCHAR(50)   | Customer first name          |
| LastName        | VARCHAR(50)   | Customer last name           |
| Phone           | VARCHAR(20)   | Phone number                 |

### Sales
| Column          | Type          | Description                  |
|----------------|---------------|------------------------------|
| SaleID         | INT PK        | Unique ID for each sale      |
| DrugID         | INT FK        | ID of the drug sold          |
| CustomerID     | INT FK        | ID of the customer           |
| Quantity       | INT           | Quantity sold                |
| SaleDate       | DATE          | Date of sale                 |

-- Create database and tables
```
SOURCE create_database.sql;

-- Insert sample data
```
SOURCE insert_data.sql;

-- Add triggers
```
SOURCE triggers.sql;

-- Test queries
```
SOURCE queries.sql;

## How to Use

1. Clone the repository:
```bash
git clone https://github.com/AnitaCloudTech/pharmacy-sales-system.git
cd pharmacy-sales-system/sql

