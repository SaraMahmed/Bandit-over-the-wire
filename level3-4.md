### 🎯 Objective

Find the password for the next level stored in a **hidden file** inside the `inhere` directory.

---

### 🧠 Concept

In Linux, **hidden files** are files whose names start with a dot (`.`).
These files are not displayed by default when using the `ls` command.

---

### 🧠 Thinking Process

1. The password is located inside a directory named `inhere`, so the first step is to move into that directory.
2. The file name is unknown, but it is hidden.
3. Since hidden files are not shown using `ls` alone, we need to use options that reveal them.

---

### 📁 Navigating to the Directory

To change the current directory:

```
cd inhere
```

---

### 📄 Listing Hidden Files

Using the regular `ls` command:

```
ls
```

No files are displayed because the file is hidden.

To list **all files including hidden ones**, use:

```
ls -al
```

This command reveals the hidden file.

---

### 📄 Reading the File

After identifying the hidden file, read its contents using:

```
cat .hidden_filename
```

(This displays the password for the next level.)

---

### 🛠 Commands Used

```
cd
ls
cat
```

---

### 🧠 Key Learning

* Hidden files start with a dot (`.`)
* `ls -al` displays all files, including hidden ones
* Navigating directories before searching is essential

---

### 📝 Notes

* Always check for hidden files when nothing appears in a directory
* Understanding `ls` options is critical for Linux navigation



---
🐧
