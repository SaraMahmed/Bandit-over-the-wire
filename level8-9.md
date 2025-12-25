### 🎯 Objective

Find the password for the next level stored in the file `data.txt`.
The password is the **only line that occurs exactly once** in the file.

---

### 🧠 Concept

When a file contains many repeated lines, finding a unique line manually is not practical.

Linux provides powerful text‑processing tools such as:

* `sort`
* `uniq`

These commands are often combined to analyze large text files efficiently.

---

### 🧠 Thinking Process

1. From the previous level, we know that `data.txt` contains a large amount of text.
2. Visual inspection is not effective.
3. The password is defined by a **property**: it appears only once.
4. The correct approach is to:

   * Sort the file
   * Filter out lines that appear more than once

---

### 🔍 Finding the Unique Line

Use the following command:

```
sort data.txt | uniq -u
```

#### Explanation:

* `sort data.txt` → groups identical lines together
* `|` (pipe) → sends the output of `sort` to `uniq`
* `uniq -u` → displays only lines that occur **once**

This command outputs the password.

---

### 🛠 Commands Used

```
sort
uniq
```

---

### 🧠 Key Learning

* Sorting text data before analysis
* Identifying unique lines in large files
* Using pipes to combine Linux commands effectively

---

### 📝 Notes

* `uniq` works correctly **only on sorted input**
* Pipes are essential for building powerful command chains
