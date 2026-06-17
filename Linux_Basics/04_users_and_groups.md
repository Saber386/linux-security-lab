# Users and Groups in Linux

## Introduction

Linux is a multi-user operating system. Every user on a Linux system has an account with specific permissions and access rights.

Users and Groups help administrators control who can access files, directories, and system resources.

---

# What is a User?

A user is an account that can log in and interact with the system.

Examples:

```text
abhinav
root
testuser
```

Each user has:

* Username
* User ID (UID)
* Home Directory
* Login Shell

---

# What is a Group?

A group is a collection of users.

Groups simplify permission management by allowing multiple users to share access to files and directories.

Example:

```text
developers
admins
sudo
users
```

---

# Viewing Current User

## whoami

Displays the currently logged-in user.

Command:

```bash
whoami
```

Output:

```text
abhinav
```

---

# Viewing User Information

## id

Displays detailed information about the current user.

Command:

```bash
id
```

Output:

```text
uid=1000(abhinav) gid=1000(abhinav) groups=1000(abhinav),27(sudo)
```

Breakdown:

```text
uid  = User ID
gid  = Group ID
groups = Groups the user belongs to
```

---

# Viewing User Groups

## groups

Displays all groups associated with a user.

Command:

```bash
groups
```

Output:

```text
abhinav sudo users
```

Meaning:

* User belongs to the sudo group
* User belongs to the users group

---

# Viewing All Users

Linux stores user information in:

```text
/etc/passwd
```

Command:

```bash
cat /etc/passwd
```

Output:

```text
root:x:0:0:root:/root:/bin/bash
abhinav:x:1000:1000:abhinav:/home/abhinav:/bin/bash
```

---

# Creating a User

## useradd

Creates a new user account.

Command:

```bash
sudo useradd testuser
```

Verify:

```bash
cat /etc/passwd
```

Output:

```text
testuser:x:1001:1001::/home/testuser:/bin/sh
```

---

# Setting a Password

## passwd

Assigns or changes a user's password.

Command:

```bash
sudo passwd testuser
```

Output:

```text
New password:
Retype new password:
passwd: password updated successfully
```

---

# Modifying a User

## usermod

Used to modify existing user accounts.

Example:

```bash
sudo usermod -aG sudo testuser
```

Meaning:

```text
-a = Append
-G = Group
```

This adds testuser to the sudo group.

---

# Deleting a User

## userdel

Removes a user account.

Command:

```bash
sudo userdel testuser
```

Delete user and home directory:

```bash
sudo userdel -r testuser
```

---

# Creating a Group

## groupadd

Creates a new group.

Command:

```bash
sudo groupadd developers
```

Verify:

```bash
cat /etc/group
```

Output:

```text
developers:x:1002:
```

---

# Adding a User to a Group

Command:

```bash
sudo usermod -aG developers testuser
```

Verify:

```bash
groups testuser
```

Output:

```text
testuser developers
```

---

# Sudo Privileges

The sudo command allows a user to execute commands with administrative privileges.

Example:

```bash
sudo apt update
```

Check sudo permissions:

```bash
sudo -l
```

---

# Practical Examples

## Example 1

Check current user:

```bash
whoami
```

Output:

```text
abhinav
```

---

## Example 2

Display user details:

```bash
id
```

Output:

```text
uid=1000(abhinav) gid=1000(abhinav)
```

---

## Example 3

Display groups:

```bash
groups
```

Output:

```text
abhinav sudo users
```

---

# Cybersecurity Relevance

Users and Groups are a critical part of Linux security.

Security professionals use them to:

* Implement Least Privilege
* Restrict access to sensitive files
* Control administrative privileges
* Prevent unauthorized access
* Manage user permissions

Common attack techniques include:

* Privilege Escalation
* User Enumeration
* Misconfigured sudo permissions

Proper user and group management helps protect Linux systems from unauthorized access.

---

# Key Takeaways

* Linux is a multi-user operating system.
* Users are individual accounts.
* Groups are collections of users.
* whoami displays the current user.
* id displays detailed user information.
* groups displays group memberships.
* useradd creates a new user.
* passwd sets a password.
* usermod modifies users and group memberships.
* userdel removes users.
* Proper user and group management improves system security.

