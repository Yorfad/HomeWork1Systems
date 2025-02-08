Hi , my proyect sistems operativs

BANKING Database Description This project implements a database to manage banking information in Microsoft SQL Server 2022. The database stores information about central banks, branches, ATMs, account holders, bank accounts and transactions. Database Structure The database consists of the following tables:

CENTRALS:
BRANCHES:
ATMS:
ACCOUNTS_HOLDERS:
ACCOUNTS:
TRANSACTIONS:
Implemented Functionalities ● Bank management: Allows registration of central banks, branches, and ATMs. ● Customer and account management: Stores information about customers and their bank accounts. ● Transaction management: Controls deposits and withdrawals through ATMs. Performance optimization: Use of indexes, partitioning and data compression to improve query efficiency. ● Security and concurrency: Enabling Snapshot Isolation to avoid deadlocks and improve data consistency. Example SQL queries To visualize the data, the following queries can be executed: SELECT * FROM CENTRALS; SELECT * FROM BRANCHES; SELECT * FROM ATMS; SELECT * FROM ACCOUNTS_HOLDERS; SELECT * FROM ACCOUNTS; SELECT * FROM TRANSACTIONS;

