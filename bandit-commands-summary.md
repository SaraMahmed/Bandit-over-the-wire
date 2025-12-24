## 🧠 General Notes

* Always inspect file type before executing it
* Use `man command` to understand available options
* Use --help to understand summary of options
* Combining commands increases efficiency and power


# Bandit Linux Commands Summary 🐧

This document summarizes the Linux commands used from **Bandit Level 0 to Level 16**, focusing on understanding their purpose and practical usage.
*to be continued*

---

## 🔐 Remote Access & Connections

### ssh

**Purpose:** Start a secure connection to a remote server.

```
ssh username@hostname -p port_number
```

**Notes:**

* Uses encrypted communication
* Commonly used for server access

---

### nc (netcat)

**Purpose:** Connect to a remote service using plaintext communication.

```
nc hostname port_number
```

**Notes:**

* Often used in CTFs
* Data is not encrypted

---

### telnet

**Purpose:** Start an unsecure remote connection.

```
telnet hostname port_number
```

**Notes:**

* No encryption
* Mostly deprecated but still useful for learning

---

### openssl

**Purpose:** Connect securely using SSL/TLS encryption.

```
openssl s_client -quiet -connect hostname:port
```

**Notes:**

* Used to inspect encrypted services
* Common in security testing

---

## 📁 File & Directory Operations

### ls

**Purpose:** List directories and files.

```
ls -al
```

**Notes:**

* `-a` shows hidden files
* `-l` shows permissions and ownership

---

### mv

**Purpose:** Move or rename files.

```
mv filename destination
mv oldname newname
```

---

### chmod

**Purpose:** Change file permissions.

```
chmod 600 filename
```

**Notes:**

* Controls read, write, and execute access

---

## 📄 File Inspection & Reading

### cat

**Purpose:** Read text files.

```
cat filename.txt
```

---

### file

**Purpose:** Identify file type.

```
file filename
```

---

### strings

**Purpose:** Display readable text from binary files.

```
strings filename
```

---

## 🔍 Searching & Filtering

### find

**Purpose:** Search for files based on different criteria.

```
find . -type f -size +1k
```

**Notes:**

* Can search by name, size, or type

---

### grep

**Purpose:** Search for specific text inside files.

```
grep "word" filename
```

---

## 🔄 Text Processing & Encoding

### sort

**Purpose:** Sort text alphabetically (A–Z).

```
sort filename
```

---

### uniq

**Purpose:** Display lines that occur only once.

```
uniq filename
```

**Notes:**

* Often used with `sort`

---

### base64

**Purpose:** Decode Base64 encoded data.

```
base64 -d filename
```

---

### tr

**Purpose:** Translate or substitute characters.

```
tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

**Notes:**

* Commonly used for ROT13 encoding/decoding

---

### xxd

**Purpose:** Convert hex dump back to binary format.

```
xxd -r oldfile newfile
```

---

## 📦 Compression & Archiving

### gzip / gunzip

**Purpose:** Compress or decompress `.gz` files.

```
gzip filename
gunzip filename.gz
```

---

### bzip2 / bunzip2

**Purpose:** Compress or decompress `.bz2` files.

```
bzip2 filename
bunzip2 filename.bz2
```

---

### tar

**Purpose:** Extract `.tar` archive files.

```
tar -xf filename.tar
```




