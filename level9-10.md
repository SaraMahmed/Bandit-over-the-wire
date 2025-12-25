### 🎯 Objective

Find the password for the next level stored in the file `data.txt` within one of the few **human‑readable strings**, preceded by several `=` characters.

---

### 🧠 Concept

The file contains **binary data**, but it also includes some readable text strings.

Linux provides the `strings` command to extract readable text from binary files.
However, this may produce many results, so additional filtering is required.

---

### 🧠 Thinking Process

1. The password is inside a **human‑readable string**, not raw binary data.
2. Using `strings` will extract all readable text.
3. The password is described as being **preceded by several `=` characters**.
4. To narrow the output, we filter the results using `grep`.

---

### 🔍 Extracting and Filtering Strings

Use the following command:

```
strings data.txt | grep "="
```

#### Explanation:

* `strings data.txt` → extracts readable text from the binary file
* `|` (pipe) → passes the output to the next command
* `grep "="` → filters lines containing `=` characters

The resulting output reveals the password.

---

### 🛠 Commands Used

```
strings
grep
```

---

### 🧠 Key Learning

* Extracting readable text from binary files
* Combining commands using pipes
* Filtering output based on specific patterns

---


