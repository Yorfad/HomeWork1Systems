Description
This project implements a database for the management of banking information in Microsoft SQL Server 2022. The BANKING database stores information about central banks, branches, ATMs, account holders, bank accounts and transactions.

Database Structure
The database is composed of the following tables:
1. CENTRALS: Contains information on central banks.
2. BRANCHES: Contains information on the branches associated with each central bank.
3.	ATMS: Records the automatic teller machines (ATMs) associated with each branch.
4.	ACCOUNTS_HOLDERS: Stores information about bank account holders.
5.	ACCOUNTS: Records the bank accounts associated to each holder and branch.
6.	TRANSACTIONS: Stores bank transactions such as deposits and withdrawals.
Each table has well defined relationships through foreign keys to ensure data integrity.

Translated with DeepL.com (free version)

Installation
Prerequisites
● Microsoft SQL Server 2022 installed and running.
● SQL Server Management Studio (SSMS) or any SQL Server compatible client.

Installation Steps
Create the database by executing
CREATE DATABASE [BANKING]
GO
1. USE [BANKING] GO
2.	Create the tables by executing the SQL commands provided.
3.	Insert test data with the INSERT INTO commands.
4.	Create indexes to optimize the search speed.
5.	Implement data partitioning in the transaction table.
6.	Enable data compression for storage optimization.
7.	Configure memory optimizations and transaction isolation to improve performance.

Functionalities Implemented
● Management of banking entities: Allows registration of central banks, branches and ATMs.
● Customer and account management: Stores customer information and their bank accounts.
● Transaction management: Controls deposits and withdrawals through ATMs.
Performance optimization: Use of indexes, partitioning and data compression to improve query efficiency.
● Security and concurrency: Enabling Snapshot Isolation to avoid deadlocks and improve data consistency.

Example SQL Queries
To visualize the data, the following queries can be executed:
SELECT * FROM CENTRALS;
SELECT * FROM BRANCHES;
SELECT * FROM ATMS;
SELECT * FROM ACCOUNTS_HOLDERS;
SELECT * FROM ACCOUNTS;
SELECT * FROM TRANSACTIONS;
