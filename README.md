# Password Manager with GUI in Python

This is a Python-based password manager that allows users to securely store and manage their passwords with encryption. The application features a graphical user interface (GUI) built with `tkinter`, and it supports adding, searching, generating, and exporting passwords. Passwords are encrypted and saved locally, ensuring data security.

## Features

- **Encryption**: Passwords are encrypted using the `cryptography` library, ensuring that sensitive data remains secure.
- **Password Generation**: Generate random, secure passwords based on customizable settings (including uppercase, lowercase, digits, and special characters).
- **Add Passwords**: Add new passwords for accounts, usernames, and optional notes. Each password is securely stored after encryption.
- **Password Search**: Search for stored passwords by account or username to quickly retrieve specific entries.
- **Export/Import Passwords**: Export passwords to a CSV file for backup and import passwords from CSV to restore them.
- **Password Strength Highlighting**: Weak passwords (less than 8 characters) are highlighted in red in the interface.
- **Copy Password to Clipboard**: Double-click a password to copy it securely to the clipboard.

## Libraries Used

- `tkinter`: For creating the graphical user interface.
- `cryptography`: For encrypting and decrypting passwords.
- `csv`: For reading and writing passwords to a CSV file.
- `random` & `string`: For generating secure passwords.

## Usage

- **Add a New Password**: 
  - Fill in the account name, username, password, and optional notes.
  - Click the "Add Password" button to save the entry.
  
- **Generate a Secure Password**: 
  - Click the "Generate New Password" button to create a password with customizable options (such as including uppercase letters, digits, and special characters).
  - The generated password will be automatically inserted into the password field.

- **Search for a Password**: 
  - Use the search bar to filter stored passwords by account or username.
  - Click the "Search" button to view the filtered list.

- **Export and Import Passwords**: 
  - Click the "Export Passwords" button to save all stored passwords to a `passwords.csv` file.
  - Use the "Import Passwords" button to load passwords from a CSV file into the application.

- **Copy Password to Clipboard**: 
  - Double-click any password entry in the password list to copy the decrypted password to your clipboard.
  - A success message will be shown confirming that the password has been copied.

---

## Security Notes

- **Encryption**: 
  - Passwords are encrypted using the `cryptography` library and a randomly generated key stored in a file called `secret.key`.
  - This encryption ensures that even if someone gains access to the password storage file (`passwords.csv`), they won't be able to read your passwords without the encryption key.

- **Password Storage**: 
  - Passwords are stored in the `passwords.csv` file in an encrypted format.
  - The `secret.key` file is necessary for decrypting the passwords.

- **First-Time Setup**: 
  - When you run the application for the first time, a new encryption key will be generated, and a file named `secret.key` will be created in the application directory.
  - **Important**: Make sure to back up the `secret.key` file. If it is lost, you won't be able to decrypt your passwords.

- **Backup**: 
  - Regularly back up both the `passwords.csv` and `secret.key` files to ensure you don't lose access to your data.

