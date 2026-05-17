# secure-password-generator
A lightweight Python script to generate strong, customizable passwords


# 🔑 Strong Password Generator

A lightweight, customizable Python script designed to generate highly secure, random passwords. Perfect for safeguarding your digital accounts without relying on third-party online generators.

---

## 🚀 Features
* **Custom Length:** Generate passwords of any desired length.
* **Character Variety:** Automatically includes uppercase letters, lowercase letters, numbers, and special symbols.
* **Highly Secure:** Uses cryptographically secure pseudo-random number generation (via Python's built-in `secrets` module) rather than standard `random`, making the passwords incredibly difficult to predict.
* **User-Friendly:** Simple command-line interface that copies the generated password straight to your clipboard (optional feature).

---

## 📦 Dependencies and Prerequisites

This project is built using Python. Depending on how your code is written, here is what is required:

### 1. Python Version
* **Python 3.6+** is required (because the script utilizes the `secrets` module introduced in Python 3.6).

### 2. Libraries Used
* **Built-in Libraries** (No installation needed):
  * `string` — For processing character sets.
  * `secrets` — For secure random number generation.
* **External Libraries** (Required *only* if your code copies text to the clipboard or formats output):
  * `pyperclip` (Optional: Used for copying passwords to the clipboard).

> 💡 **Note to Visitors:** If you are using external libraries like `pyperclip`, you will need to install them before running the script.

### Installation of Dependencies
To install the required external libraries, run the following command in your terminal:
```bash
pip install pyperclip
