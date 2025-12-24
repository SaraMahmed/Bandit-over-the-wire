## Bandit Level 0

💡 Overview

Bandit is a Linux wargame designed to teach basic and advanced Linux concepts through hands-on practice.
Each level provides a **password** that allows access to the **next level**.

The game consists of **33 levels**, and every level introduces new Linux commands or concepts.

---

 🎯 Objective

Learn how to use **SSH** to connect to a remote server.

---

🔐 Connecting to Bandit (Level 0)

To connect to the Bandit server from your virtual machine, use the following command:

```
ssh bandit0@bandit.overthewire.org -p 2200
```

* **Username:** bandit0
* **Host:** bandit.overthewire.org
* **Port:** 2200

---

🔑 Password

The password for **Level 0** is provided by the game:

```
bandit0
```

After logging in successfully, you will gain access to **Level 1**.

---

📝 Important Notes

* In each level, the **username changes** to match the current level
  (e.g. `bandit1`, `bandit2`, etc.).
* Always **save passwords locally** in a text file to avoid restarting from the beginning.
* Remember that you are working on a **remote machine**, not your local system.

---

🧠 Key Concept Learned

* Secure remote access using **SSH**
* Understanding how to connect to a Linux server using credentials

---

🛠 Command Used

```
ssh
```

**Skill Gained:** Linux Basics, Remote Access, SSH


