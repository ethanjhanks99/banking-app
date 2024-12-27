# Banking Application

## Functional Requirements
#### Account Management:

* Create a new bank account with a unique account number.
* Delete an existing bank account.
* Retrieve and display details of an existing bank account.

#### Transaction Management:

* Deposit money into an account.
* Withdraw money from an account (with checks to prevent overdrawing).
* Display the current balance of an account.

#### Data Persistence:

* Store account and transaction details in a database (e.g., SQLite).
* Load account data from the database on application start.
* Save changes to the database upon application exit or after each transaction.

## Non-Functional Requirements
#### User Interface:

* Provide a clear and user-friendly console interface.
* Display error messages and prompts for user actions.

#### Performance:

* Ensure quick retrieval and update of account information.

#### Security:

* Validate user inputs to prevent invalid transactions (e.g., negative deposits, excessive withdrawals).
* Implement basic security checks (e.g., verifying account existence before transactions).

## Optional Features
#### Account Types:

* Support different types of accounts (e.g., savings, checking) with different rules (e.g., interest rates, withdrawal limits).

#### Transaction History:

* Maintain and display a history of transactions for each account.

#### Interest Calculation:

* Calculate and apply interest to accounts periodically.

#### Multi-User Support:

* Allow multiple users to have separate accounts within the same application.

## Technical Requirements
#### Language:

* Implement the application in C++.

#### Database:

* Use SQLite for data persistence.

#### Libraries/Frameworks:

* Utilize relevant C++ libraries for database interaction (e.g., SQLiteCpp, SQLite3).

#### Version Control:

* Use Git for version control of the project.

#### Documentation:

* Document the code and provide clear instructions for building and running the application.

## Development Tasks
#### Project Setup:

* Initialize a new C++ project with necessary dependencies.

#### Database Setup:

* Design the database schema for storing account and transaction data.
* Create necessary database tables.

#### Core Features Implementation:

* Implement account creation, deletion, and retrieval.
* Implement deposit and withdrawal functionalities.
* Implement balance checking.

#### User Interface:

* Develop a console-based user interface for interacting with the application.
 
#### Data Persistence:

* Integrate SQLite for data storage and retrieval.

#### Testing:

* Write and execute tests to ensure the correctness of each feature.
* Conduct user testing to ensure the usability of the console interface.

#### Documentation:

* Write comprehensive documentation for the project, including a user guide and developer guide.
