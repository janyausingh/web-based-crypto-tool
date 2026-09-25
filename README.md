# 🔐 Web Crypto Tool

A modern, browser-based encryption and decryption tool that allows users to securely process text and files directly in their browser using the **Web Crypto API**.

The application supports both **AES-GCM symmetric encryption** and **RSA-OAEP asymmetric encryption**, along with RSA key generation, key import/export, password-strength analysis, file encryption/decryption, and convenient copy, paste, and download functionality.

> **Privacy-focused:** Cryptographic operations are performed entirely on the client side. No application server is required to process your data.

---

## ✨ Features

* 🔒 **AES-GCM Encryption & Decryption**
* 🔑 **RSA-OAEP Encryption & Decryption**
* 🗝️ **RSA 2048-bit key pair generation**
* 📁 **File encryption and decryption**
* 📤 **RSA public/private key import**
* 📥 **RSA public/private key export**
* 🔐 **Password-based AES encryption**
* 💪 **Password strength indicator**
* 📋 **Copy encrypted/decrypted output**
* 📌 **Paste directly from clipboard**
* ⬇️ **Download encrypted/decrypted files**
* 🖱️ **Drag & drop file support**
* 🌐 **Runs directly in the browser**
* 📱 **Responsive user interface**
* 🎨 **Modern dark-themed interface**
* ℹ️ **Built-in algorithm information**
* ⚠️ **Security warnings and usage guidance**

The interface provides separate Encrypt and Decrypt operations and allows users to select between AES-GCM and RSA-OAEP.

---

## 🔐 Supported Algorithms

### AES-GCM

AES-GCM is used for symmetric encryption.

The application derives a 256-bit AES key from the supplied password using:

* **PBKDF2**
* **SHA-256**
* **100,000 iterations**
* **AES-256-GCM**
* Random **16-byte salt**
* Random **12-byte initialization vector (IV)**

The generated salt and IV are stored together with the encrypted data so that the data can later be decrypted with the correct password.

### RSA-OAEP

RSA-OAEP provides asymmetric encryption using a public/private key pair.

The application generates:

* **2048-bit RSA keys**
* **RSA-OAEP**
* **SHA-256**
* Public key for encryption
* Private key for decryption

RSA keys can also be exported and imported as JSON/JWK data.

---

## 🖥️ Interface

The application provides a simple workflow:

```text
Choose Operation
       ↓
Encrypt / Decrypt
       ↓
Choose Algorithm
       ↓
AES-GCM / RSA-OAEP
       ↓
Enter Password or Manage Keys
       ↓
Enter Text / Upload File
       ↓
Process
       ↓
Encrypted / Decrypted Output
```

The UI includes dedicated input and output areas, file upload controls, copy/download buttons, and RSA key management sections.

---

## 📁 File Encryption

The tool supports encrypting and decrypting files directly in the browser.

### Encrypt a File

1. Select **Encrypt**.
2. Select **AES-GCM** or **RSA-OAEP**.
3. Enter the required password or RSA public key.
4. Upload a file or drag and drop it into the input area.
5. Click **Encrypt**.
6. Download the encrypted file.

Encrypted files are downloaded with the `.enc` extension.

### Decrypt a File

1. Select **Decrypt**.
2. Select the algorithm used during encryption.
3. Provide the correct password or RSA private key.
4. Upload the encrypted file.
5. Click **Decrypt**.
6. Download the recovered file.

---

## 🔑 RSA Key Management

When RSA-OAEP is selected, the application allows users to generate a new RSA key pair.

The generated keys can be:

* Viewed in the application
* Exported as JSON files
* Imported from JSON files
* Used for encryption and decryption

The public key is intended for encryption, while the private key should be kept confidential and used for decryption.

---

## 💪 Password Strength Meter

For AES-GCM encryption, the application includes a password-strength indicator.

The strength calculation considers:

* Password length
* Lowercase characters
* Uppercase characters
* Numbers
* Special characters

The interface categorizes passwords from **Very Weak** through **Very Strong**.

> For sensitive information, use a strong and unique password.

---

## 🔒 Privacy & Security

This project is designed around client-side processing.

The application warns users that:

> **Data is processed entirely in the browser and is not sent to a server.**

This means the application does not require a backend server for its cryptographic operations.

### Important

* Never share your AES password.
* Never share your RSA private key.
* Keep exported private keys secure.
* Losing your password or private key may prevent decryption.
* Use strong, unique passwords for sensitive data.

---

## 🛠️ Technologies Used

| Technology     | Purpose                  |
| -------------- | ------------------------ |
| HTML5          | Application structure    |
| CSS3           | Custom styling           |
| JavaScript     | Application logic        |
| Web Crypto API | Cryptographic operations |
| Tailwind CSS   | UI styling               |
| Font Awesome   | Icons                    |
| Google Fonts   | Typography               |
| File API       | File processing          |
| Clipboard API  | Copy/paste functionality |

The project uses Tailwind CSS, Font Awesome, and the Inter font through external resources.


