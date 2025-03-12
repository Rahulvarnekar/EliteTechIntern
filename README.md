# EliteTechIntern

This repository conrains 5 different tools for cyber security and digital foreniscs

File integrity checker

Web application vulnerability scanner

Penetration testing tool

Advanced encryption tool

📌Tool 1- File integrity checker

It monitors changes in a directory by computing SHA-256 hashes of files. It detects if files have been modified, added, or deleted.

How does it works?

Reads the file in chunks (to handle large files efficiently).

Computes a SHA-256 hash of the file’s contents.

Returns a unique hexadecimal hash (like a fingerprint).

If the file doesn’t exist, it prints an error.

📌Tool 2- Web application vulnerability scanner

It is a web vulnerability scanner that tests for SQL Injection (SQLi) and Cross-Site Scripting (XSS) by injecting common attack payloads into web forms.

How it works

Sends a GET request to the target URL.

Uses BeautifulSoup to extract all elements from the webpage.

Returns a list of forms found on the page.

📌Tool 3- Penetration testing tool a basic penetration testing toolkit with three main functionalities:

Port Scanner – Scans a target for open ports.

SSH Brute Force – Tries to guess an SSH password from a list.

HTTP Status Checker – Checks if a website is online.

🔹 How it works For port scanner

Uses the socket module to create a TCP connection.

Tries to connect to each port provided in the list.

If a port responds, it is considered open.

Useful for: Checking which services (SSH, HTTP, etc.) are running on a target.

🔹 How it works For SSH Brute force

Uses Paramiko (Python SSH library) to attempt logging in to SSH.

Reads passwords from a password list file and tries them one by one.

If login is successful, it prints the username and password.

If too many attempts are made, it stops (to avoid IP bans).

🔹 How it works For HTTP status checker

Sends a GET request to a given URL.

If the request is successful, it prints the HTTP status code (e.g., 200 OK).

If the request fails, it prints an offline message.

📌Tool 4- Advanced encryption tool

The script generates a 256-bit (32-byte) AES key and stores it in a file named aes_key.key. If the key file already exists, it loads the key instead of regenerating it.

How does it works? For encryption*

Read the file as plaintext.

Generate a random IV (Initialization Vector) (16 bytes) for security.

Create an AES cipher using CBC mode and the previously loaded key.

Pad the plaintext so its length is a multiple of 16 bytes (AES block size).

Encrypt the plaintext using the cipher.

Save the IV + encrypted data to a new file (filename.enc).

For decryption

Read the encrypted file.

Extract the IV (first 16 bytes) and the ciphertext (remaining bytes).

Create an AES cipher using the same key and CBC mode.

Decrypt the ciphertext.

Remove padding (last byte indicates padding length).

Save the decrypted data as the original file.
