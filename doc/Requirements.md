# Bank Account Management Application Requirements Analysis

* Basic requirements
  * Tools
    * This program will use PostgreSQL to store data
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

