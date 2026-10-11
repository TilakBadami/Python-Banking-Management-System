# Python Banking Management System

## Project Overview

The **Python Banking Management System** is a menu-driven backend application developed using Python and Object-Oriented Programming (OOP). It simulates basic banking operations, including opening bank accounts, depositing money, withdrawing money, checking balances, and displaying account details.

The system supports Savings and Current accounts, each with its own account-specific functionality. It also includes input validation to handle invalid customer details, phone numbers, account numbers, and transaction amounts.

This project was developed and tested in Jupyter Notebook as a practical implementation of Python classes, inheritance, encapsulation, method overriding, and conditional logic.

## Objectives

- Develop a basic banking application using Python.
- Implement Object-Oriented Programming concepts.
- Manage Savings and Current accounts.
- Perform deposit and withdrawal operations.
- Apply account-specific banking rules.
- Validate user input and handle invalid entries.
- Display account information and updated balances.

## Technologies Used

- **Programming Language:** Python
- **Development Environment:** Jupyter Notebook
- **Concepts:** Object-Oriented Programming, inheritance, method overriding, conditional statements, loops, functions, dictionaries, and exception handling.

## Features

### 1. Account Management
- Open a new Savings or Current account.
- Generate sequential account numbers starting from 1001.
- Require a minimum initial deposit of ₹1,000.
- Store account objects in a Python dictionary during program execution.

### 2. Deposit Money
- Deposit a positive amount into an existing account.
- Display a success message and the updated balance.
- Reject zero or negative deposit amounts.

### 3. Withdraw Money
- Withdraw money from an existing account.
- Enforce the minimum balance requirement of ₹1,000 for the general and Savings account behavior.
- Allow Current accounts to use an overdraft facility up to ₹5,000 below zero.
- Reject invalid withdrawal amounts and transactions exceeding the applicable limits.

### 4. Balance Inquiry
- Retrieve an account using its account number.
- Display the current account balance.

### 5. Account Details
Display the following information:
- Account number
- Customer name
- Phone number
- Account type
- Current balance
- Minimum balance

### 6. Savings Account Interest
- Apply a configurable interest rate of 4% in the implemented Savings account class.
- Calculate interest based on the current balance.
- Add the calculated interest to the balance.

### 7. Current Account Overdraft
- Set an overdraft limit of ₹5,000.
- Override the withdrawal method to implement Current account withdrawal rules.
- Display the overdraft limit.

### 8. Input Validation
The application validates:
- Non-empty customer names containing letters and spaces.
- Ten-digit phone numbers beginning with 6, 7, 8, or 9.
- Positive account numbers.
- Positive transaction amounts.
- A minimum opening deposit of ₹1,000.
- Valid account type and menu selections.
- Numeric input using exception handling.

## Object-Oriented Programming Concepts

| Concept | Implementation |
|---|---|
| Classes and Objects | `Bank`, `BankAccount`, `SavingsAccount`, and `CurrentAccount` |
| Inheritance | Savings and Current accounts inherit from `BankAccount` |
| Constructor | `__init__()` initializes account information |
| `super()` | Reuses the parent class constructor |
| Method Overriding | `CurrentAccount` overrides `withdraw()` |
| Encapsulation | Account data and operations are grouped within classes |
| Polymorphism | The withdrawal operation behaves differently for account types |

## Application Menu

The program provides the following options:

1. Open New Account
2. Deposit Money
3. Withdraw Money
4. Check Balance
5. Account Details
6. Add Interest (Savings)
7. Check Overdraft Limit (Current)
8. Exit

## Sample Execution

The following examples are based on the project's test runs.

### Savings Account

- Customer: Tilak
- Account number: 1001 in the first demonstrated account-creation example
- Initial deposit: ₹10,000
- Deposit: ₹2,000
- Withdrawal: ₹1,000
- Interest rate: 4%

The balance after these operations is ₹11,440.

### Current Account

- Customer: Karan
- Account number: 1002 in the demonstrated example
- Initial deposit: ₹20,000
- Deposit: ₹5,000
- Withdrawal: ₹23,000
- Remaining balance: ₹2,000
- Overdraft limit: ₹5,000

The application also rejects invalid phone numbers, invalid account-type selections, and non-numeric deposit input.

*Note: Account numbers and balances depend on the sequence of operations performed during each notebook session.*

## Project Structure

```text
Python-Banking-Management-System/
│
├── Banking_Management_System.ipynb
├── README.md
│
└── screenshots/
    ├── savings_account.png
    ├── current_account.png
    └── input_validation.png
```

## How to Run

1. Clone or download this repository.
2. Open Jupyter Notebook or JupyterLab.
3. Open `Banking_Management_System.ipynb`.
4. Execute the notebook cells in order.
5. Use the displayed menu to perform banking operations.

No external Python packages are required for the core functionality shown in this project.

## Limitations and Future Improvements

The current version is an educational simulation. Account information is stored in memory and is not preserved after the program terminates.

Potential improvements include:

- Store account information in SQLite or MySQL.
- Add transaction history and transaction IDs.
- Implement fund transfers between accounts.
- Add customer authentication and secure account access.
- Add unit tests for deposit, withdrawal, interest, and validation.
- Build a graphical user interface or web-based front end.
- Improve monetary calculations using Python's `Decimal` type.

## Conclusion

This project demonstrates the practical use of Python and Object-Oriented Programming to build a basic banking application. It provides hands-on experience with class design, inheritance, method overriding, user input validation, exception handling, and transaction logic.

**Project Type:** Python Backend Project  
**Domain:** Banking and Financial Applications  
**Author:** Tilak S Badami
