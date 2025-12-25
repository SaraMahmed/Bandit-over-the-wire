## 🧠 General Notes

* Always inspect file type before executing it
* Use `man command` to understand available options
* Use `--help` to see a quick summary of options
* Combining commands increases efficiency and power

---

# 🐧 Bandit Linux Commands Summary

This document summarizes the Linux commands used from **Bandit Level 0 to Level 16**, focusing on understanding their purpose and practical usage.
*To be continued…*

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

## 👤 User Information

### whoami

**Purpose:** Display the current logged-in user.

```
whoami
```

**Notes:**

* Very useful when dealing with permissions
* Helps confirm which user you are acting as

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

### cd

**Purpose:** Change the current directory.

```
cd directoryname
```

---

### mkdir

**Purpose:** Create a new directory.

```
mkdir directoryname
```

**Notes:**

* Used to organize files
* Helpful when creating working directories (e.g. under `/tmp`)
* `mkdir -p` creates parent directories if they do not exist

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
* Required when working with SSH private keys

---

## 📄 File Inspection & Reading

### cat

**Purpose:** Read text files.

```
cat filename.txt
```

---

### nano

**Purpose:** Edit or create text files from the terminal.

```
nano filename
```

**Notes:**

* Simple and beginner-friendly text editor
* Commonly used to edit config files or save SSH keys
* `Ctrl + O` to save, `Ctrl + X` to exit

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

* Can search by name, size, type, user, or permissions

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

* Often used after `sort`

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

