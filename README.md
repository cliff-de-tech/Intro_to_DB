# Intro_to_DB

A MySQL database project for an online bookstore system.

## Description

This project demonstrates database design and implementation for an online bookstore called **alx_book_store**. It includes database schema creation, table definitions, and data manipulation scripts.

## Database Schema

### Database Name: `alx_book_store`

### Tables

1. **Authors** - Stores information about book authors
   - `author_id` (Primary Key)
   - `author_name` VARCHAR(215)

2. **Books** - Stores information about books available in the bookstore
   - `book_id` (Primary Key)
   - `title` VARCHAR(130)
   - `author_id` (Foreign Key referencing Authors)
   - `price` DOUBLE
   - `publication_date` DATE

3. **Customers** - Stores customer information
   - `customer_id` (Primary Key)
   - `customer_name` VARCHAR(215)
   - `email` VARCHAR(215)
   - `address` TEXT

4. **Orders** - Stores information about customer orders
   - `order_id` (Primary Key)
   - `customer_id` (Foreign Key referencing Customers)
   - `order_date` DATE

5. **Order_Details** - Stores details of books in each order
   - `orderdetailid` (Primary Key)
   - `order_id` (Foreign Key referencing Orders)
   - `book_id` (Foreign Key referencing Books)
   - `quantity` DOUBLE

## Files

- **alx_book_store.sql** - Complete database and table creation script
- **MySQLServer.py** - Python script to create the database programmatically
- **task_2.sql** - Script to create all tables
- **task_3.sql** - Script to list all tables in the database
- **task_4.sql** - Script to show the full description of the Books table
- **task_5.sql** - Script to insert a single customer record
- **task_6.sql** - Script to insert multiple customer records

## Requirements

- MySQL Server
- Python 3.x
- mysql-connector-python package

## Installation

1. Install MySQL Server on your system

2. Install Python MySQL connector:
```bash
pip install mysql-connector-python
```

## Usage

### Using Python Script

1. Update the MySQL credentials in `MySQLServer.py`:
```python
user='your_username',
password='your_password'
```

2. Run the script:
```bash
python MySQLServer.py
```

### Using SQL Scripts

1. Create the database and tables:
```bash
mysql -u root -p < alx_book_store.sql
```

2. Create tables only:
```bash
mysql -u root -p alx_book_store < task_2.sql
```

3. List all tables:
```bash
mysql -u root -p alx_book_store < task_3.sql
```

4. Show Books table description:
```bash
mysql -u root -p alx_book_store < task_4.sql
```

5. Insert single customer:
```bash
mysql -u root -p alx_book_store < task_5.sql
```

6. Insert multiple customers:
```bash
mysql -u root -p alx_book_store < task_6.sql
```

## Author

Lois Adu Yeboah

## Repository

GitHub repository: `Intro_to_DB`
