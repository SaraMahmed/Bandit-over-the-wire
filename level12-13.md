### 🎯 Objective

The password for the next level is stored in the file `data.txt`, which is a **hexdump of a file that has been repeatedly compressed**.

This level focuses on learning how to **identify and handle different compressed file formats**.

---

### 🧠 Strategy Overview

1. Create a safe working directory under `/tmp`
2. Convert the hexdump back into a binary file
3. Detect the file type
4. Rename the file with the correct extension
5. Decompress it
6. Repeat until the file becomes human-readable (ASCII text)

---

### 📁 Step 1: Create a Temporary Working Directory

Instead of guessing a directory name, we use:

```
mktemp -d
```

This creates a unique directory under `/tmp`.

Then copy the file:

```
cp ~/data.txt .
```

---

### 🔄 Step 2: Convert Hexdump Back to Binary

The file is a **hexdump**, not the real binary file.

To restore it:

```
xxd -r data.txt newdata
```

Now `newdata` is a binary file.

---

### 🔍 Step 3: Identify the Compression Type

We don’t know which compression method was used, so we use:

```
file newdata
```

The output may indicate:

* gzip compressed data
* bzip2 compressed data
* POSIX tar archive

---

### ✏ Step 4: Rename the File Based on Its Type

Compression tools expect proper file extensions.

Examples:

```
mv newdata newdata.gz
mv newdata newdata.bz2
mv newdata newdata.tar
```

(The extension depends on the output of the `file` command.)

---

### 📦 Step 5: Decompress the File

Depending on the type:

**Gzip**

```
gunzip newdata.gz
```

**Bzip2**

```
bunzip2 newdata.bz2
```

**Tar**

```
tar -xf newdata.tar
```

---

### 🔁 Step 6: Repeat the Process

After each decompression:

1. Run `file` on the new output
2. Rename it correctly
3. Decompress again

Repeat until `file` shows:

```
ASCII text
```

---

### 📖 Step 7: Read the Password

Once the file becomes human-readable:

```
cat filename
```

This reveals the password for the next level.

---
### 🛠 Commands Used

```
mktemp
mkdir
cp
mv
file
xxd
gzip / gunzip
bzip2 / bunzip2
tar
```

---

### 🧠 Key Learnings

* How to reverse a hexdump using `xxd`
* How to identify file types using `file`
* How to handle multiple compression formats
* Why correct file extensions matter
* How to safely work inside `/tmp`

---

### 📝 Notes

* Always use `file` before guessing how to extract
* Multiple layers of compression are common in CTF challenges
* `/tmp` is ideal for experiments and temporary work

