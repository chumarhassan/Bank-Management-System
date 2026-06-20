# 🏦 Bank Management System

A polished, console-based Java application that simulates core banking operations for administrators and customers via an ATM-like interface.

---

## ✨ At a Glance
- Create and manage accounts
- Check balances, withdraw, deposit, and transfer funds
- Admin tools: view accounts, update PINs, delete accounts
- Secure PIN validation with temporary lockout on repeated failures
- Persistent account storage via text-based records (AllAccountsDetails.txt)

---

## 🧩 Key Components
- Main method: entry point offering Bank or ATM modes with a persistent interaction loop
- bank(): Admin and new-user flows; account creation and administrative actions
- atm(): Card + PIN authentication, balance checks, withdrawals, transfers
- Transactions: checkBalance(), withdrawCash(), transferMoney()
- Admin tools: adminBank() — summaries, searches, PIN updates, deletions
- Utilities: isAccountExists(), accountNumberExists(), updatePinInFile(), deleteUserDetails()
- File I/O: all account data persisted to `AllAccountsDetails.txt`

---

## 🚀 Quickstart (Run locally)
1. Build & run with Java (JDK 8+):

```bash
javac Main.java
java Main
```

2. Follow console prompts to choose Bank or ATM mode.

Tip: keep `AllAccountsDetails.txt` in the same folder as the program for persistence.

---

## 🔐 Security & Validation
- PIN attempts are limited; repeated failures trigger a temporary lockout
- Account numbers and card numbers are validated to prevent collisions
- Input is validated; invalid choices are handled with user-friendly messages

---

## 🗂 File Layout (example)
- src/ — Java source files (Main.java, Bank.java, ATM.java, Utils.java)
- data/ — `AllAccountsDetails.txt` (persisted account data)
- README.md — this file

---

## 🛠️ Troubleshooting
- FileNotFound: ensure `AllAccountsDetails.txt` exists or the app has write permission
- Invalid input loops: restart the app after correcting malformed data in the data file
- PIN lockout: wait the cooldown period or have admin reset PIN via bank admin menu

---

## 🧭 Design Notes
- Modular methods improve readability and testability
- Simple text-file persistence keeps dependencies minimal; migrate to a DB (SQLite/MySQL) for production
- Consider adding logging and unit tests for robustness

---

## 🤝 Contributing
1. Fork
2. Create a branch: `git checkout -b feat/ui-improvements`
3. Implement and test changes
4. Open a PR describing your enhancement

---

## 📬 Questions & Feedback
Open an issue in this repo with steps to reproduce and expected behavior.

---
