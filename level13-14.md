### 🎯 Level Goal

The password for the next level is stored in
`/etc/bandit_pass/bandit14`
and can **only** be read by user `bandit14`.

Instead of a password, you are given a **private SSH key** that allows you to log in as `bandit14`.

---

## 🧠 Core Idea

This level teaches how to:

* Use an **SSH private key** instead of a password
* Understand **file permissions**
* Authenticate as another user using SSH key-based login

---
## 🔍 Step 1: Confirm Current User

Check which user you are logged in as:

```
whoami
```

Output:

```
bandit13
```

So you **cannot** read `/etc/bandit_pass/bandit14` directly.

---

## 🔑 Step 2: Locate the Private SSH Key

List files in the home directory:

```
ls -al
```

You will find a file containing the private key (usually named something like `sshkey.private`).

Read it:

```
cat sshkey.private
```

---

## 💾 Step 3: Copy the Key to Your Local Machine because in bandit you will not be able to create a nwe ssh inside old one so you have to exit first 

1. Select and copy the entire private key content
2. Exit the Bandit server

On your **local machine**:

```
nano bandit14.key
```

Paste the key content and save the file.

---

## 🔐 Step 4: Fix Key Permissions

SSH **refuses** to use private keys with open permissions.

Set correct permissions:

```
chmod 600 bandit14.key
```

This means:

* Read & write for owner only
* No permissions for group or others

---

## 🔗 Step 5: Login Using the SSH Key

Now log in as `bandit14`:

```
ssh -i bandit14.key -p 2220 bandit14@bandit.overthewire.org
```

✔ No password required
✔ Authentication is done using the private key

---

## 📖 Step 6: Read the Password

Once logged in:

```
cat /etc/bandit_pass/bandit14
```

This gives you the password for the next level.

---

## 🧠 Key Learnings

* SSH can authenticate using **keys instead of passwords**
* Private keys must have **strict permissions**
* `ssh -i` specifies a private key file
* You cannot bypass Linux permissions without proper authentication
* SSH keys are commonly used in servers, DevOps, and CTFs

---
## 🛠 Commands Used

```
whoami
ls
cat
chmod
ssh
nano
```

---
## ⚠ Important Notes

* SSH ignores keys with permissions higher than `600`
* Never share private SSH keys
* Always verify the current user with `whoami`
