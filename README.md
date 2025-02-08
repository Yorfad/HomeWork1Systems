# BANKING Database

This project implements a database for the management of banking information in Microsoft SQL Server 2022. The BANKING database stores information about central banks, branches, ATMs, account holders, bank accounts, and transactions.

---

## Structure of the database

The database consists of the following tables:

1. **CENTRALS**: contains information on central banks.
2. **BRANCHES**: contains information on the branches associated with each central bank.
3. **ATMs**: records the teller machines (ATMs) associated with each branch.
4. **ACCOUNTS_HOLDERS**: stores information on bank account holders.
5. **ACCOUNTS**: records the bank accounts associated with each account holder and branch.
6. **TRANSACTIONS**: stores bank transactions, such as deposits and withdrawals.

Each table has well-defined relationships using foreign keys to ensure data integrity.

---

## Installation

### Prerequisites

- Microsoft SQL Server 2022 installed and running.
- SQL Server Management Studio (SSMS) or any SQL Server compatible client.

### Installation Steps

1. Create the database by running:
   ```sql
   CREATE DATABASE [BANKING]
   GO
   ```
2. Use the database:
   ```sql
   USE [BANKING]
   ```
3. Create the tables by executing the SQL commands provided.
4. Insert test data with the `INSERT INTO` commands.
5. Create indexes to optimize search speed.
6. Implement data partitioning in the transaction table.
7. Enable data compression for storage optimization.
8. Configure memory optimizations and transaction isolation to improve performance.

---

## Functionalities Implemented

- **Bank management**: Allows registration of central banks, branches, and ATMs.
- **Customer and account management**: Stores information on customers and their bank accounts.
- **Transaction management**: Controls deposits and withdrawals via ATMs.
- **Performance optimization**: Use of indexes, partitioning, and data compression to improve query efficiency.
- **Security and concurrency**: Enabling Snapshot Isolation to avoid deadlocks and improve data consistency.

---

## Example SQL Queries

To display the data, the following queries can be executed:

```sql
SELECT * FROM CENTRALS;
SELECT * FROM BRANCHES;
SELECT * FROM ATMS;
SELECT * FROM ACCOUNTS_HOLDERS;
SELECT * FROM ACCOUNTS;
SELECT * FROM TRANSACTIONS;
