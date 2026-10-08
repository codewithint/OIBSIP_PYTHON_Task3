# Random Password Generator — Python Desktop App

A feature-rich desktop application for creating secure, randomized passwords using Python and Tkinter. The application provides flexible password customization, real-time strength evaluation, clipboard integration, local password history, and customizable themes through a simple graphical interface.

## ✨ Key Features

- **Secure Password Creation:** Uses Python's `secrets` module to generate unpredictable passwords.
- **Adjustable Length:** Choose any password length between 8 and 64 characters.
- **Flexible Character Selection:** Customize passwords using:
  - Capital letters (A–Z)
  - Small letters (a–z)
  - Digits (0–9)
  - Special symbols
- **Character Selection Validation:** Requires uppercase letters and at least one additional character category.
- **Ambiguous Character Filter:** Optionally removes characters that are easily confused, such as `O`, `0`, `l`, and `1`.
- **Strength Evaluation:** Displays a visual indication of password strength based on length and character variety.
- **Quick Copy Function:** Copies generated passwords using `pyperclip`, with a Tkinter clipboard fallback.
- **Local Password Records:** Stores recent password entries in an SQLite database.
- **Recent History Limit:** Retains only the five newest generated passwords.
- **History Management:** Review previous entries, copy individual passwords, or remove saved history.
- **Dual Appearance Modes:** Switch between light and dark themes.
- **Scrollable Interface:** Navigate the application comfortably within a compact desktop window.
- **Standalone Storage:** Uses a local SQLite database without requiring a separate database server.

## 🛠️ Built With

| Technology | Purpose |
|---|---|
| Python 3 | Core application logic |
| Tkinter | Desktop interface and interactive controls |
| SQLite | Local storage for password history |
| `secrets` | Cryptographically secure random selection |
| `string` | Standard character collections |
| `pathlib` | Database and filesystem path handling |
| `pyperclip` | Clipboard operations |

## 📋 Prerequisites

Before starting, make sure your system has:

- Python 3 installed.
- Tkinter available in your Python installation.
- Git installed if you intend to clone the repository.
- The dependencies specified in `requirements.txt`.

## 🚀 Installation Guide

### Step 1: Download the project

Clone the repository and move into its directory:

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd OIBSIP_Python_Task3
```

### Step 2: Install dependencies

Install the packages required by the application:

```bash
python -m pip install -r requirements.txt
```

### Step 3: Launch the application

Start the desktop password generator:

```bash
python main.py
```

The application window should open, allowing you to configure and generate passwords.

## 📖 How to Use

1. **Set the length:** Select a value between 8 and 64 characters.
2. **Configure character sets:** Open the Character Type section and enable uppercase letters plus at least one other category.
3. **Improve readability:** Enable the ambiguous-character exclusion option if desired.
4. **Generate a password:** Click Generate Password to create a new password.
5. **Copy the result:** Use the copy button or the automatic clipboard feature when available.
6. **Check previous entries:** Visit History to view or copy one of the five most recent passwords.
7. **Manage saved data:** Use Clear History when you want to remove stored password records.
8. **Personalize the interface:** Open Settings and choose your preferred theme.

## 🔐 Password Storage and Privacy

Password history is maintained locally in a database named `password_history.db`, created automatically when the application runs.

Important security considerations:

- The database stores generated passwords in readable form.
- Anyone who obtains access to the database may be able to read the saved passwords.
- Avoid storing important account credentials in the application's history.
- Use a reputable password manager for long-term credential storage.
- Clear the history when saved entries are no longer needed.
- Keep `password_history.db` excluded from Git commits through `.gitignore`.

The application does not require an external database service for its local history functionality.

## 📊 Password Strength Rules

The application estimates password strength using password length and the number of enabled character categories.

| Condition | Displayed strength |
|---|---|
| 16+ characters with all 4 character types | Strong |
| 14+ characters with at least 3 types | Strong |
| 12+ characters with at least 3 types | Medium |
| 10+ characters with at least 2 types | Medium |
| Other valid combinations | Weak |

*Note:* This is a simplified indicator rather than a complete measure of password security. Actual security also depends on randomness, uniqueness, and resistance to guessing.

## 📁 Directory Structure

The project is organized into the following files:

```text
RANDOM PASSWORD GENERATOR/
├── .gitignore
├── README.md
├── main.py
└── requirements.txt
```

The `password_history.db` file is generated automatically at runtime. It should remain excluded from version control to reduce the risk of exposing saved passwords.

## 👨‍💻 Developer

**Dani Sarkar**

A Python desktop application project focused on secure password generation, practical usability, and local data management.
