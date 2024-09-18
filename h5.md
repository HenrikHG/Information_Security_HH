# h5 Uryyb, Greb!

---

## Summary of Schneier 2015: "Applied Cryptography: Chapter 1 - Foundations"

- **Introduction to Cryptography**: 
  - Cryptography is a method used to secure communication in the presence of adversaries.
  - It relies on mathematical algorithms to encode and decode information.
  
- **Cryptographic Systems**:
  - Cryptographic systems can be divided into two main categories: symmetric-key (private-key) and asymmetric-key (public-key).
  - **Symmetric-key Cryptography**:
    - Uses the same key for both encryption and decryption.
    - Fast and suitable for large amounts of data, but requires a secure way to share the key.
  - **Asymmetric-key Cryptography**:
    - Uses a pair of keys: a public key (for encryption) and a private key (for decryption).
    - Solves the key distribution problem but is slower compared to symmetric-key systems.

- **Cryptographic Algorithms**:
  - Cryptographic algorithms provide various functionalities, including encryption, decryption, and hashing.
  - Examples of cryptographic algorithms include DES (Data Encryption Standard), RSA (Rivest-Shamir-Adleman), and SHA (Secure Hash Algorithm).

- **Cryptanalysis**:
  - The science of breaking cryptographic codes.
  - Attackers use different techniques such as brute force, frequency analysis, and more advanced mathematical methods.

- **Foundational Concepts**:
  - **Confidentiality**: Ensuring that information is not accessible to unauthorized parties.
  - **Integrity**: Ensuring that the data has not been altered in an unauthorized way.
  - **Authentication**: Verifying the identity of the entities involved in communication.
  - **Non-repudiation**: Guaranteeing that a sender cannot deny sending the message.

- **Historical Perspective**:
  - Cryptography has evolved from simple techniques like the Caesar cipher to complex algorithms.
  - Modern cryptography involves computer algorithms and mathematical principles to create secure communication methods.

---

## Summary of Karvinen 2023: "PGP - Send Encrypted and Signed Message - gpg"

- **PGP**: Encrypts and signs messages using public/private keys.
- **Setup**: Install `gpg` (`sudo apt-get install gpg`). Generate keys (`gpg --gen-key`).
- **Key Sharing**: Export public key (`gpg --export`). Share it for encrypted messaging.
- **Encrypt/Decrypt**: Use recipient's public key to encrypt. Use your private key to decrypt.
- **Verify**: Always check public key fingerprints.
- **Troubleshooting**: Reset `gpg-agent` if needed.

-> You can find an detailed instruction how to use PGP in the next task

---

# a) Pretty Good Indeed - Encryption and Decryption Guide

## 1. Installation

First, install `gpg` and any other necessary tools:

```bash
sudo apt-get update
sudo apt-get install gpg micro psmisc
```

![Screenshot (13)](https://github.com/user-attachments/assets/17452a2f-1040-4b41-8e24-70dea64c489b)

## 2. Generate Your Keypair

To create a keypair (which includes a public and private key):

```bash
gpg --gen-key
```

Provide your full name and email address when prompted. You can choose not to set a password for this key, though it’s more secure to do so. To see the details of your keypair, use:

![Screenshot (15)](https://github.com/user-attachments/assets/f3110831-40ba-4cc8-b4ec-1260c33612ac)

```bash
gpg --fingerprint
```

You will see the public key ID and other details.

![Screenshot (16)](https://github.com/user-attachments/assets/8922352e-8662-4634-8e74-b31be26ea684)

## 3. Export Your Public Key

To allow others to send you encrypted messages, you need to share your public key:

```bash
gpg --export --armor --output mypublickey.pub
```

This command creates an ASCII armored public key file named `mypublickey.pub`.

![Screenshot (17)](https://github.com/user-attachments/assets/a09fbebb-617d-44cd-af53-bbb0a90ff8be)

## 4. Simulate a second user (Alice)

![Screenshot (18)](https://github.com/user-attachments/assets/6e5e57c0-c94a-4ff7-a05b-be66c5690aab)

![Screenshot (19)](https://github.com/user-attachments/assets/d97d7a40-b8f3-4c2c-aa8e-2b5bb7133a2e)


## 5. Import and Trust a Public Key (as Alice)

Before we import we will copy the key to alice folder

```bash
cd
cp -v mypblickey.pub alice/
```

Import the public key:

```bash
cd alice/
gpg -- homedir . -- import mypublickey.pub
```

To verify the fingerprint of the imported key:

```bash
gpg --homedir . --fingerprint
```

![Screenshot (21)](https://github.com/user-attachments/assets/a51d62a4-8d66-45ff-9d6a-8308ef9cf6dd)

Once verified, mark the key as trusted:

```bash
gpg --homedir . --sign-key "KEY_ID"
```

Replace `KEY_ID` with the key's fingerprint or email address.

![Screenshot (23)](https://github.com/user-attachments/assets/a3aaf2e1-133d-4807-8f57-88680ded91ed)

## 5. Encrypt a Message

Create a message

![Screenshot (28)](https://github.com/user-attachments/assets/1cf9681a-1fa2-460f-bdd6-a33127319b07)

To encrypt a message for a recipient, you need their public key. Assuming you’ve already imported and trusted their key, run:

```bash
gpg --encrypt --recipient recipient@example.com --armor --output encrypted_message.pgp message.txt
```

Here:
- `--recipient` specifies the email associated with the recipient's public key.
- `--armor` outputs the message in ASCII format for easier handling.

![Screenshot (29)](https://github.com/user-attachments/assets/13b56e9d-bc1a-4043-afdb-9b121d469007)

## 6. Decrypt a Message

Send the message file - or move it to the right folder in our example.

![grafik](https://github.com/user-attachments/assets/a6986937-3938-445e-9165-847c447636fd)

If you receive an encrypted message, use your private key to decrypt it:

```bash
gpg --decrypt encrypted_message.pgp
```

You should see the original message content, and `gpg` will verify the signature if the sender has signed the message.

![grafik](https://github.com/user-attachments/assets/8b97cbd2-75f8-4ad7-8306-73c0fa2510b5)

---

# b) Password Manager

## KeePass Password Safe - Installation and Usage Guide

**KeePass Password Safe** is a free, open-source password manager that allows you to securely store all your passwords in a local, encrypted database file. It does not require cloud storage, keeping your sensitive information safe on your device. 

### Why Use a Password Manager?

A password manager like KeePass is necessary for managing complex and unique passwords for each of your accounts. Here are some reasons why you need it:

- **Protection Against Common Attacks**:
  - **Brute Force Attacks**: Complex passwords are harder to crack. KeePass can generate strong, random passwords that are nearly impossible to guess.
  - **Phishing Attacks**: With KeePass, you don’t have to manually type passwords, reducing the risk of accidentally entering credentials into fake sites.
  - **Keylogging**: KeePass has an auto-type feature that enters usernames and passwords directly, bypassing keyloggers that could otherwise record your keystrokes.
- **Avoiding Password Reuse**: Using the same password for multiple accounts increases the risk of a breach. KeePass enables you to generate and manage unique passwords for every service.
- **Data Privacy**: KeePass does not rely on cloud storage, so your passwords are stored locally on your device, reducing exposure to remote hacking attempts.

### Installing KeePass Password Safe

Follow these steps to install KeePass on your Windows system:

1. **Download KeePass**:
   - Go to the official KeePass website: [https://keepass.info/](https://keepass.info/).
   - Navigate to the "Downloads" section and choose "KeePass 2.x" (recommended for most users).

2. **Install KeePass**:
   - Run the downloaded installer (`KeePass-2.xx-Setup.exe`).
   - Follow the on-screen instructions to complete the installation.
   - Once installed, open KeePass.

### Using KeePass Password Safe

### Step 1: Creating a New Database

1. Open KeePass.
2. Click on **File > New** to create a new password database.

![Screenshot (35)](https://github.com/user-attachments/assets/83d4826d-bc43-43ba-9128-532cfb0fdf42)

3. Choose a location on your local drive to save the database (e.g., `MyPasswords.kdbx`).

![Screenshot (36)](https://github.com/user-attachments/assets/c749fa83-b65e-4fb7-8fdb-56f5d92510ce)

4. Set a **master password** for your database. This is the only password you need to remember, so make it strong and unique.
5. You can optionally configure a key file for additional security.

![Screenshot (37)](https://github.com/user-attachments/assets/5b2b4b45-cbe9-4269-9bae-197bc168dd36)

### Step 2: Adding Entries (Passwords)

1. With the database open, right-click on a group (e.g., "General") or create a new group.
2. Select **Add Entry**.
3. Fill in the details:
   - **Title**: Name of the service (e.g., "Google Account").
   - **Username**: Your username or email.
   - **Password**: Generate a strong password using the password generator (click on the three dots to open the generator).
   - **URL**: Optional, for quick access to the login page.
   - **Notes**: Additional information if needed.
4. Click **OK** to save the entry.

![Screenshot (40)](https://github.com/user-attachments/assets/d67999d4-8a5b-4dbe-9616-d010a065a3a2)

