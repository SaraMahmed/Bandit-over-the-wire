### 🎯 Objective

Read the password for the next level from a file named:

```
--spaces in this filename--
```

located in the home directory.

---

### 🧠 Concept

Linux treats **spaces** in file names as **separators between arguments**, not as part of the file name.
Additionally, `--` at the beginning of a file name can affect how commands interpret options:

* `--` signals the end of command options, so anything after it is treated as an argument (like a file name), even if it starts with `-`.

---

### 🧠 Thinking Process

To read the file, you need to handle:

1. **Double dash (`--`) at the start**
2. **Spaces in the file name**

---

### 📄 Solutions

#### Option 1: Escape spaces with `\`

```
cat -- --spaces\ in\ this\ filename--
```

* `--` tells Linux that options are finished
* `\` escapes each space so it's treated as part of the file name

---

#### Option 2: Use quotes

```
cat -- "--spaces in this filename--"
```

* Double quotes keep the whole string together
* `--` still handled correctly

---

### ⚠️ Important Note

* Using `cat ./--spaces in this filename--` **will not work** because spaces are still interpreted as separate arguments, even though `./` handles the `--`.

---

### 🛠 Commands Used

```
cat
```

---

### 🧠 Key Learning

* Handling filenames with **spaces**
* Understanding **double dash (`--`)** to terminate options
* Escaping characters vs quoting strings in Linux

---

### 📝 Notes

* Always check how Linux interprets special characters in filenames
* Quoting or escaping is essential when working with unusual file names

---


