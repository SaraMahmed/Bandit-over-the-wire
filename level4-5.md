### 🎯 Objective

Find the password for the next level stored in the **only human‑readable file** inside the `inhere` directory.

---

### 🧠 Concept

Not all files contain readable text.
Some files may be binary, compressed, or encoded.

A **human‑readable file** usually appears as **ASCII text** when inspected.

---

### 🧠 Thinking Process

1. Navigate into the `inhere` directory.
2. List all files, but their names alone do not indicate which one contains readable text.
3. Identify the file type of each file to determine which one is human‑readable.

---

### 📁 Navigating to the Directory

```
cd inhere
```

---

### 📄 Identifying File Types

To check the content type of **all files at once**, use:

```
file ./*
```

This command applies `file` to every file in the directory.

The file that appears as:

```
ASCII text
```

is the target file.

---

### 📄 Reading the File

Once identified, read the file using:

```
cat filename
```

This reveals the password for the next level.

---

### 🛠 Commands Used

```
cd
file
cat
```

---

### 🧠 Key Learning

* File extensions are not reliable indicators of file content
* The `file` command helps identify readable vs binary files
* Wildcards (`*`) can apply commands to multiple files at once

---

### 📝 Notes

* If the terminal output becomes unreadable, use:

  ```
  reset
  ```
* Always inspect files before reading or executing them

