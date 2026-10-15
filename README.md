<div align="center">

# 🏦 Bank Management System

**A lightweight, interactive console application for managing customers and bank accounts — built in C++.**

![Language](https://img.shields.io/badge/Language-C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![Interface](https://img.shields.io/badge/Interface-CLI-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white)
![Storage](https://img.shields.io/badge/Storage-In--Memory-orange?style=for-the-badge)
![Purpose](https://img.shields.io/badge/Purpose-Educational-blueviolet?style=for-the-badge)

[Overview](#-overview) •
[Features](#-key-features) •
[Quick Start](#-quick-start) •
[Usage](#-using-the-application) •
[Architecture](#-how-it-works) •
[Roadmap](#-roadmap)

</div>

---

## 📖 Overview

Welcome! 👋 The **Bank Management System** simulates the day-to-day operations of a bank teller through a clean, menu-driven command-line interface.

Bank staff can register customers, open accounts, and process deposits and withdrawals — all without a database or external service. Everything runs **in memory**, making the project fast to set up, easy to read, and ideal for learning core C++ concepts such as:

- 🧱 Structs and data modelling
- 📦 STL containers (`std::vector`)
- 🔁 Menu-driven control flow
- ✅ Input handling and validation

---

## ✨ Key Features

| Feature | Description |
|:--|:--|
| 👤 **Add Customer** | Register a customer with an ID, name, address, and contact information |
| 🏧 **Create Account** | Open a new account linked to an existing customer ID |
| 🔢 **Auto Account Numbers** | Each account receives a unique, sequentially generated number |
| 💰 **Deposit** | Add funds to any existing account |
| 💸 **Withdraw** | Withdraw funds with built-in **insufficient-balance protection** |
| 📋 **Display Accounts** | View a complete summary of every account in the system |
| 🚪 **Graceful Exit** | Close the application cleanly at any time |

---

## 🚀 Quick Start

Get up and running in under a minute.

### ✅ Prerequisites

- A C++ compiler such as **g++** (GCC), **clang++**, or **MSVC**

### 🐧 Linux / 🍎 macOS

```bash
# 1. Compile
g++ main.cpp -o bank_management_system

# 2. Run
./bank_management_system
```

### 🪟 Windows

```cmd
:: 1. Compile
g++ main.cpp -o bank_management_system.exe

:: 2. Run
bank_management_system.exe
```

> 💡 **Tip:** Add `-std=c++17 -Wall` to the compile command to use a modern standard and see helpful compiler warnings.

---

## 🎮 Using the Application

When the program starts, you'll see the main menu:

```text
----- Bank Management System -----
1. Add Customer
2. Create Account
3. Deposit
4. Withdraw
5. Display Accounts
0. Exit
Enter your choice:
```

| Option | Action | What you'll need |
|:--:|:--|:--|
| `1` | Add Customer | Customer ID, name, address, contact info |
| `2` | Create Account | An existing customer ID and account type |
| `3` | Deposit | Account number and amount |
| `4` | Withdraw | Account number and amount |
| `5` | Display Accounts | — |
| `0` | Exit | — |

### 🧭 Typical Workflow

```text
  Add Customer  ──▶  Create Account  ──▶  Deposit / Withdraw  ──▶  Display Accounts
     (Option 1)         (Option 2)          (Options 3 & 4)          (Option 5)
```

<details>
<summary><b>▶️ Click to see a sample session</b></summary>

<br>

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

Once the customer exists, choose **Option 2** to open an account. Use the generated **account number** for every deposit and withdrawal that follows.

</details>

---

## ⚙️ How It Works

The application keeps all data in two in-memory collections:

```text
┌─────────────────────────┐         ┌──────────────────────────┐
│       customers         │         │        accounts          │
│  (std::vector)          │  1 ── * │  (std::vector)           │
├─────────────────────────┤         ├──────────────────────────┤
│ • Customer ID           │◀────────│ • Customer ID            │
│ • Name                  │         │ • Account Number         │
│ • Address               │         │ • Account Type           │
│ • Contact Information   │         │ • Current Balance        │
└─────────────────────────┘         └──────────────────────────┘
```

- **`customers`** — stores every registered customer.
- **`accounts`** — stores every bank account, linked to its owner through the **customer ID**.

A single customer can hold multiple accounts, and every account must belong to a registered customer.

---

## 📁 Project Structure

```text
Bank-MAnagement-System-main/
├── main.cpp                 # Application source code
├── README.md                # Project documentation
└── bank_management_system   # Compiled executable (generated after build)
```

---

## 📝 Important Notes

> [!NOTE]
> Data is stored **in memory only**. All customers and accounts are cleared when the program exits.

> [!IMPORTANT]
> Withdrawals are validated — a transaction is rejected if the amount exceeds the available balance.

> [!TIP]
> Account numbers are generated **sequentially** at runtime, so note them down as you create accounts.

---

## 🗺️ Roadmap

Ideas for taking this project further:

- [ ] 💾 Persist data to a file or database
- [ ] 🔐 Add staff login and authentication
- [ ] 🔄 Support fund transfers between accounts
- [ ] 🧾 Record a transaction history for each account
- [ ] 🔍 Search for customers and accounts
- [ ] 🧪 Add unit tests

---

## 🤝 Contributing

Contributions, suggestions, and feedback are always welcome!

1. **Fork** the repository
2. **Create** a feature branch: `git checkout -b feature/your-feature`
3. **Commit** your changes: `git commit -m "Add your feature"`
4. **Push** the branch: `git push origin feature/your-feature`
5. **Open** a Pull Request 🎉

---

## 📄 License

This project is intended for **educational and learning purposes**.

<div align="center">

---

⭐ **If you found this project helpful, consider giving it a star!** ⭐

</div>
