# Bank Account Management Application High Level Design

## Table of Contents
* [Database](#database)
  * [Tables](#tables)
* [Authentication and Authorization](#authentication-and-authorization)
  * [Registration](#registration)

## Database
* Using PostgreSQL with C++
  * [Link to libpq++ dox](https://www.postgresql.org/docs/7.2/libpqplusplus.html)

### Tables
* User
  * UserId - int
  * UserName - string
  * FirstName - string
  * LastName - string
  * MidName? - string
  * SSN - hashed string
  * LastSSN - int
  * Password - hashed string
* Accounts
  * AccountId - int
  * OwnerId - int - Signifies who owns the account
  * AuthorizedUsers - int - many-to-many relationship with User
  * AccountType - string
  * Balance - float
* Transactions
  * TransId - int
  * AccountId - many-to-one relationship (Many transactions, one account)
  * Amount - float
  * Type - string

## Authentication and Authorization
* Authentication and Authorization will be implemented by two separate methods: one for registering an account, and one for logging into an account
* PostgreSQL will be used to manage user data and session information

### Registration and Authorization
* Information required for an account (\* optional):
  * First name
  * Last name
  * Username
  * Password
  * Email
  * SSN
  * Middle name \*
* Password and SSN will be hashed to protect privacy in the event of a data leak
* 
