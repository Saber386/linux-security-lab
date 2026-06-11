# Linux Navigation Commands

## Overview

Navigation commands are among the most frequently used commands in Linux. Understanding how to move through directories, inspect files, and locate resources is essential for system administration, incident response, log analysis, and cybersecurity investigations.

---

## pwd

### Purpose

Displays the current working directory.

### Syntax

```bash
pwd
```

### Example

```bash
$ pwd
/home/abhinav
```

### Cybersecurity Use Case

During incident investigations, analysts often need to verify their current location before accessing logs, malware samples, or configuration files.

---

## ls

### Purpose

Lists files and directories.

### Syntax

```bash
ls
```

### Example

```bash
$ ls
Documents Downloads Pictures
```

### Cybersecurity Use Case

Useful when examining unfamiliar systems or investigating suspicious directories.

---

## ls -la

### Purpose

Lists all files, including hidden files, with detailed information.

### Syntax

```bash
ls -la
```

### Example

```bash
$ ls -la
drwxr-xr-x 2 user user 4096 Jun 10 .
-rw-r--r-- 1 user user  128 secret.txt
```

### Cybersecurity Use Case

Hidden files may contain malware, persistence mechanisms, SSH keys, or unauthorized scripts.

---

## cd

### Purpose

Changes the current directory.

### Syntax

```bash
cd directory_name
```

### Example

```bash
cd /var/log
```

### Cybersecurity Use Case

Security analysts frequently navigate to locations such as:

```bash
/var/log
/etc
/home
/tmp
```

while performing investigations.

---

## cd ..

### Purpose

Moves one directory level up.

### Syntax

```bash
cd ..
```

### Example

```bash
/home/abhinav/projects

cd ..

/home/abhinav
```

### Cybersecurity Use Case

Useful when traversing directory structures during forensic analysis.

---

## tree

### Purpose

Displays directory structures in a tree format.

### Syntax

```bash
tree
```

### Example

```bash
project
├── logs
├── scripts
└── reports
```

### Cybersecurity Use Case

Provides a quick overview of file organization and can help identify suspicious files or directories.

---

## Summary

* pwd shows your current location.
* ls displays directory contents.
* ls -la reveals hidden files.
* cd changes directories.
* cd .. moves up one level.
* tree visualizes directory structures.

These commands form the foundation of Linux navigation and are used daily by system administrators, SOC analysts, incident responders, and cybersecurity professionals.
