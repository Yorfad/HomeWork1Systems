NATALY MICHELL CUX RECINOS 1890-22-18009

## Data Base Project for a Banking System

This repository contains a SQL script for the creation of a banking system database. The database is designed to manage banking centers, branches, ATMs, account holders, bank accounts and transactions.

## Data Base Structure

## Main Tables

1. **CENTRALS**: Stores information about the central banks.
   - central_id_central`: Unique identifier of the central.
   - name_central`: Name of the central.
   - address_central`: Address of the central.
   - phone_central`: Telephone of the control panel.
   - central_email`: Central e-mail.
   - CREATED_DATE`: Creation date of the record.
   - UPDATED_DATE`: Date of last update of the record.


2. **BRANCHES**: Stores information about bank branches.
   - id_branch`: Unique identifier of the branch.
   - code_branch`: Unique code of the branch.
   - name_branch`: Branch name.
   - address_branch`: Branch address.
   - phone_branch`: Branch phone number.
   - email_branch`: E-mail of the branch.
   - id_central_branch`: Foreign key referring to the central office to which the branch belongs.
   - CREATED_DATE`: Creation date of the record.
   - UPDATED_DATE`: Date of last update of the record.

3. **ATMs**: Stores information about the ATMs.
   - id_atm`: Unique identifier of the ATM.
   - code_atm`: Unique ATM code.
   - name_atm`: Name of the ATM.
   - address_atm`: ATM address.
   - phone_atm`: Telephone of the ATM.
   - email_atm`: E-mail of the ATM.
   - id_branch_atm`: Foreign key referring to the branch to which the ATM belongs.
   - CREATED_DATE`: Creation date of the record.
   - UPDATED_DATE`: Date of last update of the record.

4. **ACCOUNTS_HOLDERS**: Stores information about account holders.
   - id_account_holder`: Unique identifier of the account holder.
   - `name_account_holder`: Name of the account holder.
   - address_account_holder`: Address of the account holder.
   - phone_account_holder`: Account holder's phone number.
   - email_account_holder`: Account holder's email address.
   - CREATED_DATE`: Creation date of the record.
   - UPDATED_DATE`: Date of last update of the record.

5. **ACCOUNTS**: Stores information about the bank accounts.
   - `id_account`: Unique identifier of the account.
   - number_account`: Unique number of the account.
   - type_account`: Account type (SAVINGS or MONETARY).
   - currency_account`: Account currency (USD or GTQ).
   - balance_account`: Account balance.
   - id_account_holder_account`: Foreign key referring to the account holder.
   - id_branch_account`: Foreign key referring to the branch where the account was opened.
   - CREATED_DATE`: Creation date of the record.
   - UPDATED_DATE`: Date the record was last updated.


6. **TRANSACTIONS**: Stores information about the transactions performed.
   - transaction_id`: Unique transaction identifier.
   - type_transaction`: Type of transaction (DEPOSIT or WITHDRAWAL).
   - amount_transaction`: Amount of the transaction.
   - id_account_transaction`: Foreign key referring to the account involved in the transaction.
   - id_atm_transaction`: Foreign key referring to the ATM where the transaction was performed.
   - CREATED_DATE`: Creation date of the record.
   - UPDATED_DATE`: Date the record was last updated.




###  Table Relationships

- **BRANCHES** is related to **CENTRALS** through `id_central_branch`.
- ATMS** is related to **BRANCHES** through `id_branch_atm`.
- ACCOUNTS** is related to **ACCOUNTS_HOLDERS** through `id_account_holder_account` and to **BRANCHES** through `id_branch_account`.
- TRANSACTIONS** is related to **ACCOUNTS** through `id_account_transaction` and to **ATMS** through `id_atm_transaction`.



###  Indexes

Indexes have been created to improve query performance on the following columns:

- `id_central_branch` in **BRANCHES**.
- `id_branch_atm` in **ATMS**.
- `id_account_holder_account` in **ACCOUNTS**.
- `id_branch_account` in **ACCOUNTS**.
- `id_account_transaction` in **TRANSACTIONS**.
- `id_atm_transaction` in **TRANSACTIONS**.


### Views

- **AccountDetails**: View that combines account, account holder and branch information.



### Stored Procedures

- **DepositMoney**: Procedure to make a deposit to an account.



### Triggers

- **trg_AuditAccountBalance**: Trigger to audit account balance changes.



### Partitioning

- A partitioning function has been created for the **TRANSACTIONS** table based on the creation date.



### Data Compression

- Data compression has been applied to the **TRANSACTIONS** and **ACCOUNTS** tables to save space.



### Optimization

- Configured the database to use `READ_COMMITTED_SNAPSHOT` and `ALLOW_SNAPSHOT_ISOLATION` to improve performance in high concurrency environments.



## Execution 

In the attached file script_sqlServer you will find the script to run it, just copy and paste the content in a `.sql` file and run it in your SQL Server