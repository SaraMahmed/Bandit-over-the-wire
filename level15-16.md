### 🎯 Level Goal

The password for the next level can be retrieved by submitting
the password of the **current level** to **port 30001 on localhost**
using **SSL/TLS encryption**.

---

## 🧠 Core Idea

This level teaches:

* Difference between **plain text connections** and **encrypted connections**
* How to interact with an SSL/TLS service
* Using `openssl s_client` to communicate securely

---

## ❌ Why nc / telnet Will Not Work

From the previous level, we used:

* `nc`
* `telnet`

But in this level:

* The service **requires SSL/TLS**
* Plain TCP tools will fail or return unreadable output

So we must use a tool that understands **encryption**.

---

## ✅ Correct Tool: OpenSSL

### Connect to the Service

```
openssl s_client -connect localhost:30001
```

(You may also add `-quiet` to reduce output noise.)

---

## 📤 Submit the Password

After the connection is established:

* Paste the password from the **previous level**
* Press **Enter**

The server will respond with the password for the next level.

---
## 🛠 Commands Used

```
openssl
```

---
## 🧠 Key Learnings

* SSL/TLS encrypts data during transmission
* `openssl s_client` acts like a secure version of `nc`
* Many secure services cannot be accessed without encryption
* This technique is widely used in security testing and CTFs

---

## ⚠ Notes

* Always read the level description carefully
* If you see certificate info, that is normal
* Use `Ctrl + C` to exit the connection
