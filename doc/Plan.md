# C++ Bank Account Management Application Development Plan

## Phase 0: Analysis of Requirements

* Basic requirements
  * Tools
    * This program will use SQLlite to store data
    * This program will use git for version control
  * As a user, I should be able to...
    * register a bank account
    * login to my bank account
    * open new accounts (checking, savings, etc.)
    * deposit money
    * withdraw money
    * see the balance in all accounts
    * close accounts
    * close my bank account
    * view a history of transactions for each account
  * Non-functional requirements
    * User interface should be clear and user-friendly
    * Program should display errors when an invalid input is given
    * User inputs should be validated to prevent invalid transactions
    * Program should implement basic security checks
* Database Tables used by the program
  * User
    * A user has access to the functionality of the program
  * Bank Accounts
    * One user can have one bank acount
    * A bank account has one user
  * Accounts
    * An account is attatched to one bank account
    * A bank account has many accounts
  * Transactions
    * A transaction is tied to one account
    * An account has many transactions
* Algorithms
  * Deposit money into an account
  * Withdraw money from an account
  * Veiw balance from account
  * Veiw transaction history from account
  * Create an account
  * Create a bank account
  * Delete an account
  * Delete a bank account
  * Register a new bank account
  * Login to bank account

## Phase 1: Design

* Using SQLite3 with C++
  * Use `#include <sqlite3.h>`
  * [Link to examples](https://www.geeksforgeeks.org/sql-using-c-c-and-sqlite/)
  * [Link to SQL commands](https://www.sqlitetutorial.net/sqlite-cheat-sheet/)

### Authentication and Authorization

* Authentication and Authorization will be implemented by two separate methods: one for registering an account, and one for logging into an account
* SQLite will be used to manage user data and session information

#### Register

* Information required for an account:
  * First name
  * Last name
  * Username
  * Password
  * Email
  * SSN
* Password and SSN will be hashed to protect privacy in the event of a data leak
* 
