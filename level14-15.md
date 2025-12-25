### 🎯 Level Goal

The password for the next level can be retrieved by submitting
the password of the **current level** to **port 30000 on localhost**.

---

## 🧠 Core Idea

This level teaches:

* How to **send data during a network connection**
* Difference between **SSH** and **plaintext connections**
* Using **telnet** or **netcat (nc)** to interact with services

---
## ❌ Why SSH Will Not Work

Your first thought may be:

```
ssh localhost -p 30000
```

But this **will NOT work** because:

* SSH expects an **SSH service**
* SSH encrypts and handles authentication internally
* It does **not** allow sending a password as plain text after connection

The service on port `30000` is waiting for **raw input**, not SSH authentication.

---

## ✅ Correct Approach

We need a tool that:

* Opens a **plain TCP connection**
* Allows us to **manually send text**

Perfect tools:

* `telnet`
* `nc` (netcat)

---

## 🔗 Method 1: Using Telnet

```
telnet localhost 30000
```

After connection:

* Paste the password you got from **level 14**
* Press **Enter**

➡ The server will respond with the password for the next level.

---

## 🔗 Method 2: Using Netcat (Recommended)

```
nc localhost 30000
```

Then:

* Paste the password
* Press **Enter**

✔ Simpler
✔ Cleaner
✔ Commonly used in CTFs

---

## 🧠 Key Learnings

* `localhost` means **your current machine**
* Some services expect **plain text input**
* SSH is **not** for raw data submission
* `nc` and `telnet` are used for:

  * Debugging services
  * CTF challenges
  * Network testing

---
## 🛠 Commands Used

```
telnet
nc
```
---
## ⚠ Notes

* `nc` is preferred over `telnet` in modern environments
