### 🎯 Objective

Find the password for the next level stored in a file **somewhere under** the `inhere` directory with the following properties:

* Human‑readable
* Exactly **1033 bytes** in size
* **Not executable**

---

### 🧠 Concept

When files are scattered across directories and have specific properties, manual searching is inefficient.
Linux provides the `find` command to search files based on **type, size, and permissions**.

---

### 🧠 Thinking Process

1. Navigating into `inhere` and listing files is not enough.
2. Using `file ./*` only checks readability, but ignores size and executability.
3. The correct approach is to **search using multiple conditions**.
4. This is where the `find` command becomes essential.

---

### 📁 Navigating to the Directory

```
cd inhere
```

---

### 🔍 Searching by File Properties

To locate the target file, use:

```
find . -type f -size 1033c ! -executable
```

#### Explanation:

* `.` → search in the current directory and subdirectories
* `-type f` → regular files only
* `-size 1033c` → file size is exactly 1033 bytes
* `! -executable` → file is **not executable**

This command returns the file that matches **all required conditions**.

---

### 📄 Reading the File

After locating the file, read it using:

```
cat filename
```

This reveals the password for the next level.

---

### 🛠 Commands Used

```
cd
find
cat
```

---

### 🧠 Key Learning

* Searching files by **multiple properties**
* Using `find` instead of manual inspection
* Understanding file size units (`c` = bytes)
* Filtering executable vs non‑executable files

---

### 📝 Notes

* The `find` command is extremely powerful and commonly used in system administration and security
* Combining conditions reduces false results and saves time
