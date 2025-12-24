## Bandit Level 1

### 🎯 Objective

Find the password for the next level stored in a file called **readme** located in the home directory, then use it to log in to **bandit2** via SSH.

---

### 🧠 Thinking Process

Since the password is stored in a file, the first step is to **list the files** in the home directory and check whether the file exists.

---

### 📁 Listing Files

To view all files in the current directory, use:

```
ls
```

After listing the files, we can see a file named:

```
readme
```

---

### 📄 Reading the File

To read the content of the file and obtain the password, use:

```
cat readme
```

This command displays the password for the next level.

---

### 🔐 Accessing the Next Level

After obtaining the password, use SSH to log in to **bandit2**:

```
ssh bandit2@bandit.overthewire.org -p 2200
```

---

### 🛠 Commands Used

```
ls
cat
ssh
```

---

### 🧠 Key Concepts Learned

* Listing files in a directory using `ls`
* Reading file content using `cat`
* Using credentials to access the next level via SSH

---

### 📝 Notes

* Always verify file names before reading them.
* Save each level’s password locally to avoid restarting the game.
* The username always matches the level number (e.g., `bandit1`, `bandit2`).

---

**Skills Gained:** Linux Basics, File Navigation, SSH

---
