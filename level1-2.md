## Bandit Level 2

### 🎯 Objective

Read the password for the next level from a file named **`-`** located in the home directory.

---

### 🧠 Concept

In Linux, the dash (`-`) is commonly used to specify **command options**, such as:

```
ls -al
```

Because of this, Linux may interpret `-` as an option instead of a file name.

---

### 🧠 Thinking Process

Attempting to read the file using:

```
cat -
```

does not work as expected because the system treats `-` as standard input or an option.

To solve this, the file must be referenced **explicitly as a file path** so Linux understands it is a file name, not an option.

---

### 📄 Reading the File

To read the file correctly, use:

```
cat ./-
```

* `./` tells Linux to look in the **current directory**
* `-` is then treated as the file name, not an option

This command displays the password for the next level.

---

### 🛠 Commands Used

```
cat
```

---

### 🧠 Key Learning

* Linux treats `-` as a special character
* Prefixing the file name with `./` forces Linux to interpret it as a file
* Special file names require explicit paths


### 📝 Notes

* Always consider how Linux parses command arguments
* Using relative paths can prevent misinterpretation of file names

