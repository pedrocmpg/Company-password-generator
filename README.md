# 🔒 Custom Enterprise Password Generator

A secure and modern desktop application built with **Python** and **PySide6** designed to automate and standardize corporate password creation based on custom legacy business rules, featuring local storage with **SQLite**.

> 💡 **Why this exists:** This software solves a real-world infrastructure constraint: generating strong, highly memorable, and compliant passwords that fit specific corporate formatting patterns across multiple business units.

---

## 📸 Preview
*Insert a screenshot of the modern PySide6 interface here to show your UI/UX skills!*

---

## 🚀 Key Features

* **Strict Pattern Enforcement:** Guarantees every password matches the exact infrastructure rule: `[Word] + [Special Character] + [Word] + [Unit Number]` (e.g., `Garfo@Tomate02`).
* **Corporate Dictionary Integration:** Uses optimized, pre-defined local wordlists tailored for high memorability among employees.
* **Smart Collision Avoidance:** The algorithm checks the database in real-time and attempts up to 100 iterations to guarantee 100% unique credentials, preventing duplicates across units.
* **Unit-Based Organization:** Easily filter, generate, and view password history mapped to 24 distinct business units.
* **Clipboard Automation:** One-click button to copy credentials instantly to the clipboard safely.
* **Modern UI/UX:** Clean, dark-themed responsive interface designed entirely with PySide6.

---

## 💾 Database Architecture

The system automatically initializes and manages a local `senhas_geradas.db` database using SQLite. It records:
* Generated Credential
* Associated Business Unit & Unit Number
* Timestamp (Date and Time of generation)

---

## 🛠️ Technologies Used

* **Python 3.x**
* **PySide6 (Qt for Python)** - For the modern graphical user interface.
* **SQLite** - For lightweight, zero-configuration local data persistence.

---

## 🔧 Extensibility & Customization

The codebase was architected to be easily maintainable. Developers can modify the core logic to:
* Expand the core dictionary array (`self.palavras`).
* Update the allowed special characters sequence (`self.simbolos`).
* Dynamically map new business locations within the `self.unidades` dictionary.
