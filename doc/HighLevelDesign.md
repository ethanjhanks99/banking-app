
* Using SQLite3 with C++
  * Use `#include <sqlite3.h>`
  * [Link to examples](https://www.geeksforgeeks.org/sql-using-c-c-and-sqlite/)
  * [Link to SQL commands](https://www.sqlitetutorial.net/sqlite-cheat-sheet/)
* Tables
  * 

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
