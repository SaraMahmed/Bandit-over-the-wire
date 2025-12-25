### 🎯 Objective

The password for the next level is stored in the file `data.txt`, where all lowercase (a–z) and uppercase (A–Z) letters have been **rotated by 13 positions**.

---

### 🧠 Concept (ROT13)

ROT13 is a simple letter substitution cipher.
Each letter is replaced by the letter **13 positions after it** in the alphabet.

Example for lowercase letters:

```
a b c d e f g h i j k l m n o p q r s t u v w x y z
n o p q r s t u v w x y z a b c d e f g h i j k l m
```

The same logic applies to **uppercase letters**.

---

### 🧠 Thinking Process

1. The file name is known: `data.txt`.
2. The content is readable text but **encoded using ROT13**.
3. Manually replacing letters would be slow and impractical.
4. Linux provides the `tr` command, which can translate characters efficiently.

---

### 🔄 Decoding Using `tr`

We map:

* `A-Z` → `N-ZA-M`
* `a-z` → `n-za-m`

Command used:

```
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

This command outputs the decoded text, revealing the password for the next level.

---

### 🛠 Commands Used

```
tr
cat
```

---

### 🧠 Key Learning

* Understanding ROT13 substitution cipher
* Using `tr` for character translation
* Handling both uppercase and lowercase letters

---

### 📝 Notes

* ROT13 is **not encryption**, it’s a simple encoding technique
* Often used in CTFs and basic security challenges

