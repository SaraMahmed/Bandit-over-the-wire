### 🎯 Level Goal

The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000–32000**.

Steps required:

1. Find which ports in this range have a server listening
2. Determine which of them use **SSL/TLS**
3. Identify the **only server** that returns the next credentials
   (others will just echo your input)

---

## 🧠 Core Idea

This level teaches:

* **Port scanning**
* Differentiating between open and closed ports
* Detecting **SSL/TLS services**
* Combining `nmap` with `openssl`

---

## 🔍 Step 1: Scan the Port Range

We don’t know the exact port, only the range, so we scan it using `nmap`:

```
nmap localhost -p 31000-32000
```

This will show which ports are **open** and have services listening on them.

You will find a few open ports.

---

## 🔐 Step 2: Identify SSL/TLS Ports

Not all open ports use encryption.

Since the level requires **SSL/TLS**, we must test the open ports using `openssl`.

Try connecting to each open port:

```
openssl s_client -connect -quite localhost:PORT
```

Replace `PORT` with each open port number.

---

## 📤 Step 3: Submit the Password

For each successful SSL/TLS connection:

* Paste the password from the **current level**
* Press **Enter**

### Expected Behavior:

* **Wrong ports:** Echo back whatever you send
* **Correct port:** Returns the **credentials for the next level**

There is **only one correct server**.

---
## 🛠 Commands Used

```
nmap
openssl
```

---

## 🧠 Key Learnings

* Port ranges often hide services
* `nmap` is essential for reconnaissance
* SSL/TLS services require encryption-aware tools
* `openssl s_client` is used to manually interact with secure services
* Not every open port gives useful data

---

## ⚠ Notes

* Ignore certificate warnings — they are normal here
* Use `Ctrl + C` to exit `openssl`
* Always combine scanning + testing
