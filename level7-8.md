### 🎯 Objective

Find the password for the next level stored in the file `data.txt` **next to the word `millionth`**.

---

### 🧠 Concept

When dealing with **large text files**, reading the entire file manually is inefficient.

The `grep` command allows searching for specific words or patterns inside files quickly and accurately.

---

### 🧠 Thinking Process

1. The file name is known: `data.txt`.
2. The file contains a large amount of text.
3. The password is located next to a specific word.
4. Searching visually is impractical, so a text‑search command is required.

---

### 🔍 Searching Inside the File

Use the following command:

```
grep "millionth" data.txt
```

This command displays the line containing the word **millionth**, which also contains the password.

---

### 🛠 Commands Used

```
grep
```

---

### 🧠 Key Learning

* Efficient searching inside large files
* Using `grep` to locate specific words or patterns
* Avoiding manual inspection of large datasets

---

### 📝 Notes

* `grep` is case‑sensitive by default
* It is widely used in log analysis and system debugging

---
🐧
