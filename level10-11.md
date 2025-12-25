### 🎯 Objective

Find the password for the next level stored in the file `data.txt`, which contains **Base64-encoded data**.

---

### 🧠 Concept

Base64 is an encoding scheme used to represent binary data in a text format.

Reading Base64-encoded content directly using `cat` will not reveal meaningful information.
The data must be **decoded** first.

---

### 🧠 Thinking Process

1. The file name is known: `data.txt`.
2. The content appears unreadable when viewed normally.
3. The level description specifies that the data is Base64-encoded.
4. The correct approach is to **decode** the file before reading it.

---

### 🔄 Decoding the File

Use the following command:

```
base64 -d data.txt
```

This command decodes the content and reveals the password for the next level.

---

### 🛠 Commands Used

```
base64
```

---

### 🧠 Key Learning

* Understanding Base64 encoding
* Decoding encoded data using Linux tools
* Recognizing when data needs transformation before reading

---

### 📝 Notes

* Base64 is encoding, **not encryption**
* Encoded data often appears in emails, APIs, and configuration files


