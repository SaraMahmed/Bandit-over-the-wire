### 🎯 Objective

Find the password for the next level stored **somewhere on the server** with the following properties:

* Owned by user **bandit7**
* Owned by group **bandit6**
* Exactly **33 bytes** in size

---

### 🧠 Concept

When the file location is unknown and permissions vary across the system, searching manually is not practical.

The `find` command allows searching files by:

* Owner
* Group
* Size

It also allows redirecting error messages to avoid cluttering the output.

---

### 🧠 Thinking Process

1. The file can exist anywhere on the server, so the search must start from the root directory.
2. Multiple search conditions are required (user, group, size).
3. Searching the entire system will result in many **permission denied** errors.
4. These error messages can be suppressed by redirecting them.

---

### 🔍 Searching the Entire Server

Use the following command:

```
find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

#### Explanation:

* `/` → search the entire filesystem
* `-type f` → regular files only
* `-user bandit7` → file owner
* `-group bandit6` → group owner
* `-size 33c` → file size is 33 bytes
* `2>/dev/null` → suppress permission denied error messages

---

### 📄 Reading the File

After locating the file, read it using:

```
cat filename
```

This displays the password for the next level.

---

### 🛠 Commands Used

```
find
cat
```

---

### 🧠 Key Learning

* Searching files by **ownership**
* Handling permission errors gracefully
* Redirecting **stderr** to `/dev/null`
* Efficient system‑wide file searching

---

### 📝 Notes

* `2>` refers to **standard error (stderr)**
* `/dev/null` discards unwanted output
* This technique is widely used in scripting and system administration

