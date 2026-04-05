#  Cryptography Basics

##  Introduction

Cryptography is the practice of securing information by transforming it into an unreadable format so that only authorized users can access it. It plays a critical role in cybersecurity by ensuring data confidentiality, integrity, and authenticity.

---

#  Types of Encryption

##  1. Symmetric Encryption

###  Definition

Symmetric encryption uses a **single key** for both encryption and decryption.

###  Working

* Plaintext is encrypted using a secret key.
* The same key is used to decrypt the ciphertext.

###  Example

If Alice and Bob share a secret key:

* Alice encrypts message using the key
* Bob decrypts using the same key

###  Algorithms

* AES (Advanced Encryption Standard)
* DES (Data Encryption Standard)

###  Advantages

* Fast and efficient
* Suitable for large data

###  Disadvantages

* Key distribution is difficult

---

##  2. Asymmetric Encryption

###  Definition

Asymmetric encryption uses **two keys**:

* Public Key (shared)
* Private Key (kept secret)

###  Working

* Data encrypted with public key
* Decrypted with private key

###  Example

* Sender uses receiver’s public key
* Only receiver can decrypt using private key

###  Algorithms

* RSA (Rivest-Shamir-Adleman)
* ECC (Elliptic Curve Cryptography)

###  Advantages

* Secure key exchange
* Used in secure communication

###  Disadvantages

* Slower than symmetric encryption

---

##  Real-World Usage

Modern systems combine both:

* Asymmetric encryption → Key exchange
* Symmetric encryption → Data transfer

---

#  Hashing

##  Definition

Hashing converts input data into a **fixed-length string (hash value)**.

###  Key Features

* One-way function (cannot be reversed)
* Same input → same hash
* Small change → completely different hash

---

##  MD5

### Features

* Produces 128-bit hash
* Fast but insecure

###  Issues

* Vulnerable to collision attacks
* Not recommended for security use

---

##  SHA-256

### Features

* Produces 256-bit hash
* Highly secure

###  Applications

* Password storage
* Blockchain
* Digital signatures

---

#  Digital Certificates & SSL/TLS

##  Digital Certificate

###  Definition

A digital certificate is an electronic document that verifies the identity of a website.

###  Contains

* Domain name
* Public key
* Certificate Authority (CA)
* Expiry date

---

##  Certificate Authority (CA)

Trusted organization that issues certificates.

### Examples

* DigiCert
* Let’s Encrypt

---

##  SSL/TLS

###  Definition

Protocols used to secure communication over the internet.

👉 HTTPS = HTTP + SSL/TLS

---

##  How SSL/TLS Works

1. Client requests secure connection
2. Server sends certificate
3. Client verifies certificate
4. Session key is generated
5. Secure communication begins

---

# 🧪 Hands-on: OpenSSL

## 🔧 Install OpenSSL

```bash
sudo apt update
sudo apt install openssl
```

---

##  Create File

```bash
echo "Hello Cybersecurity" > message.txt
```

---

##  Encrypt File

```bash
openssl enc -aes-256-cbc -salt -in message.txt -out message.enc
```

---

##  Decrypt File

```bash
openssl enc -aes-256-cbc -d -in message.enc -out decrypted.txt
```

---

##  View Decrypted Content

```bash
cat decrypted.txt
```

---

##  Generate Hash

```bash
openssl dgst -sha256 message.txt
```

---

#  Summary

| Concept               | Description          |
| --------------------- | -------------------- |
| Cryptography          | Secures data         |
| Symmetric Encryption  | One key              |
| Asymmetric Encryption | Two keys             |
| Hashing               | One-way function     |
| MD5                   | Insecure             |
| SHA-256               | Secure               |
| SSL/TLS               | Secure communication |

---

#  Real-World Applications

*  Password Storage → Hashing
*  Secure Browsing → SSL/TLS
*  Online Banking → Encryption
*  Secure Email → Asymmetric Encryption

---

#  Conclusion

Cryptography is the backbone of modern cybersecurity. Understanding encryption, hashing, and secure communication protocols is essential for protecting data from unauthorized access and attacks.
