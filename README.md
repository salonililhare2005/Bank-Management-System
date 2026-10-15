# Bank Management System

A simple, interactive console-based C++ application for managing customer records and bank accounts. This project demonstrates core banking operations such as customer registration, account creation, deposits, withdrawals, and account listing using in-memory storage.

## Overview

The application provides a command-line interface (CLI) for bank staff to perform essential banking tasks without requiring a database or external service. All customer and account data are managed in memory while the program is running.

## Key Features

- Add a new customer with:
  - Customer ID
  - Name
  - Address
  - Contact information
- Create a new bank account for an existing customer using their customer ID
- Automatically assign a unique account number for each account
- Deposit money into an account
- Withdraw money from an account with balance validation
- Display all account details in the system
- Exit the application gracefully

## Main Menu

The application presents the following menu at startup:

1. Add Customer
2. Create Account
3. Deposit
4. Withdraw
5. Display Accounts
0. Exit

## How It Works

The project uses two in-memory vectors:

- `customers`: stores all registered customers
- `accounts`: stores all bank accounts and their balances

Each account contains:

- Account number
- Customer ID
- Account type
- Current balance

## Example Workflow

```text
----- Bank Management System -----
1. Add Customer
2. Create Account
3. Deposit
4. Withdraw
5. Display Accounts
0. Exit
Enter your choice: 1
Enter customer ID: 101
Enter name: John Smith
Enter address: 21 Market Street
Enter contact information: +1 555 123 4567
CUSTOMER ADDED SUCCESSFULLY!
```

After creating a customer, the user can create an account and then perform deposit or withdrawal operations using the generated account number.

## Run the Project

### Compile

Using a C++ compiler such as `g++`:

```bash
g++ main.cpp -o bank_management_system
```

### Run

```bash
./bank_management_system
```

On Windows:

```cmd
g++ main.cpp -o bank_management_system.exe
bank_management_system.exe
```

## Notes

- This project uses in-memory storage only; data is not saved permanently to a file or database.
- The application validates insufficient balance before allowing withdrawals.
- Account numbers are generated sequentially during runtime.

## Project Structure

```text
Bank-MAnagement-System-main/
├── main.cpp
├── README.md
└── compiled executable (generated after build)
```

## License

This project is intended for educational and learning purposes.

