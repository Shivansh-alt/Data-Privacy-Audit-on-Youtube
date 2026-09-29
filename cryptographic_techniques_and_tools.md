# Cryptographic Techniques and Tools

Cryptography is used to **protect information** from unauthorized access and to verify its authenticity. Three important techniques are:

| Technique | Purpose | Common algorithms/tools |
|---|---|---|
| **Encryption** | Protects confidentiality; data can be recovered using a key | AES, RSA, OpenSSL |
| **Hashing** | Creates a fixed-length fingerprint; one-way operation | SHA-256, SHA-3, Argon2id |
| **Digital Signature** | Verifies authenticity, integrity, and the sender's identity | RSA, ECDSA, Ed25519 |

## 1. Encryption

Encryption converts **plaintext → ciphertext** using a key.

```text
Plaintext → Encryption + Key → Ciphertext
Ciphertext → Decryption + Key → Plaintext
```

### Python Example

Using Python's `cryptography` library:

```python
from cryptography.fernet import Fernet

key = Fernet.generate_key()
cipher = Fernet(key)

message = b"Hello World"

encrypted = cipher.encrypt(message)
decrypted = cipher.decrypt(encrypted)

print("Encrypted:", encrypted)
print("Decrypted:", decrypted.decode())
```

Here, the same secret key is used for encryption and decryption.

---

## 2. Hashing

Hashing converts data into a **fixed-length hash value**. Unlike encryption, a cryptographic hash is designed to be **one-way**.

```text
"Hello World" → SHA-256 → 64-character hexadecimal hash
```

### Python Example

```python
import hashlib

message = b"Hello World"

hash_value = hashlib.sha256(message).hexdigest()

print(hash_value)
```

Even a small change in the input produces a substantially different hash.

> **Note:** Passwords should generally be stored using password-specific algorithms such as **Argon2id**, rather than plain SHA-256.

---

## 3. Digital Signatures

A digital signature uses a **private key to sign** data. Others can use the corresponding **public key to verify** the signature.

```text
Message + Private Key → Digital Signature

Message + Signature + Public Key → Valid / Invalid
```

### Python Example

```python
from cryptography.hazmat.primitives.asymmetric import ed25519

private_key = ed25519.Ed25519PrivateKey.generate()
public_key = private_key.public_key()

message = b"Hello World"

signature = private_key.sign(message)

# Verify the signature
public_key.verify(signature, message)

print("Signature is valid")
```

If the message is modified after signing, verification fails.

---

## Summary

| Technique | Main Purpose |
|---|---|
| **Encryption** | Confidentiality |
| **Hashing** | Integrity / Fingerprinting |
| **Digital Signature** | Authenticity + Integrity |

### Common Cryptographic Tools

- **Python `cryptography`** — Cryptographic operations in Python
- **OpenSSL** — Command-line cryptographic toolkit
- **GPG/GnuPG** — Encryption and digital signatures
- **Platform cryptographic libraries** — Cryptographic functions provided by operating systems and programming environments
