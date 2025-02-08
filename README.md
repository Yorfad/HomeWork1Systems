BANKING Database

////////////////////////////////////////////////////////Description////////////////////////////////////////////////////////
This is a project of a data management system for banks, focused on optimizing data storage and querying in a way that is easy to use without compromising any essential functionality.
Database Structure
The database is composed of the following tables:
1. CENTRALS: Contains information on the most important central or banks.
2. BRANCHES: Contains information about the branches associated with each central bank.
3.	ATMS: Records the multiple cash registers associated with each central or branch.
4.	ACCOUNTS_HOLDERS: Stores information about the Clients.
5.	ACCOUNTS: Records the bank accounts associated to each client and branch.
6.	TRANSACTIONS: Stores bank transactions such as deposits and withdrawals.
Each table has well defined relationships using foreign keys to store the information.

////////////////////////////////////////////////////////Installation////////////////////////////////////////////////////////
Prerequisites
● Microsoft SQL Server 2022 installed and running.
● SQL Server Management Studio (SSMS) or any SQL Server compatible client.

////////////////////////////////////////////////////////Installation Steps////////////////////////////////////////////////////////
Create the database by running:
CREATE DATABASE [BANKING]
GO
1. USE [BANKING].
2.	Create the tables by executing the SQL commands provided.
3.	Insert test data with the INSERT INTO commands.
4.	Create indexes to optimize the search speed.
5.	Implement data partitioning in the transaction table.
6.	Enable data compression for storage optimization.
7.	Configure memory optimizations and transaction isolation for performance improvement.

////////////////////////////////////////////////////////Implemented Functionalities/////////////////////////////////////////////////////
● Bank management: Improved the way of consulting information from the central and branch offices.
● Customer and account management: Stores customer and bank account information.
● Transaction management: Controls deposits and withdrawals through ATMs.
● Performance optimization: Use of indexes, partitioning and data compression to improve query efficiency.
● Security and concurrency: Enabling Snapshot Isolation to avoid deadlocks and improve data consistency.
Improvements and Modifications Made.
● Partitioning of the TRANSACTIONS table: We partition the transactions table to be able to store large volumes of data in a compressed way, mainly for old data to be able to store it securely and take up less space.
● Compression of data in ACCOUNTS and TRANSACTIONS to optimize storage usage and optimize query load times for these.
● Indexes in key columns for improved search performance.
● AccountDetails view to quickly and easily obtain detailed account information with account holders.

////////////////////////////////////////////////////////Example SQL Queries////////////////////////////////////////////////////////
To visualize to make the database work correctly we can execute the following scripts:
SELECT * FROM CENTRALS;
SELECT * FROM BRANCHES;
SELECT * FROM ATMS;
SELECT * FROM ACCOUNTS_HOLDERS;
SELECT * FROM ACCOUNTS;
SELECT * FROM TRANSACTIONS;
