# 🔑 Advanced CLI Password Generator

A secure, terminal-based password generation tool written in Python. By leveraging cryptographic hashing, Key Derivation Functions (KDF), and secure token generation, this script creates strong, unpredictable passwords right from your command line.

---

## 📖 Introduction & Overview

This tool is designed for users who want complete control over their digital security without relying on third-party password managers or online generators. It runs **100% locally** on your machine, ensuring your master keys and generated passwords never touch the internet.

Given the architecture of the script, it functions as a highly secure utility that can handle:
* **Masked Inputs:** Keeping your master passwords safe from shoulder-surfers.
* **Cryptographic Hashing:** Turning simple inputs into high-entropy, complex keys.
* **Native Clipboard Integration:** Seamlessly passing your new password to your system clipboard for instant use.

---

## 📦 Dependencies & Technical Breakdown

One of the best features of this script is that it features **zero external Python dependencies**. It relies entirely on Python's robust Standard Library. You do not need to run `pip install` to get started.

Here is how the script utilizes your system's resources based on its imports:

| Module | Classification | Purpose in This Script |
| :--- | :--- | :--- |
| `secrets` | Cryptography | Generates cryptographically secure random numbers tokens, far safer than the standard `random` module. |
| `hashlib` & `hmac` | Cryptography | Handles secure hashing algorithms (like SHA-256) and Keyed-Hashing for message authentication. |
| `getpass` | Security / UI | Secures the terminal interface by hiding/masking your password keystrokes as you type them. |
| `base64` & `string` | Data Formatting | Translates raw cryptographic bytes into readable alphanumeric characters and symbols. |
| `subprocess` | System Integration | Interacts with your operating system's native clipboard utility to copy passwords automatically. |
| `os`, `sys`, `re` | System / Logic | Manages command-line arguments, environment paths, and complex text pattern matching (Regex). |

### 🐧 System Prerequisites (Linux Users Only)
While Python requires no extra packages, your operating system might. If the clipboard feature utilizes tools like `xclip` or `xsel` under the hood via the `subprocess` module, Linux users may need to install it utility via their package manager:

```bash
# For Ubuntu / Debian / Mint:
sudo apt install xclip

# For Fedora:
sudo dnf install xclip

# For Arch Linux:
sudo pacman -S xclip
