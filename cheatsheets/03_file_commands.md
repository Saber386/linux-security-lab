# Linux File Commands 

This cheat sheet contains commonly used Linux file and directory management commands for quick reference.

---

## Navigation

| Command          | Purpose                           |
| ---------------- | --------------------------------- |
| `pwd`            | Display current working directory |
| `ls`             | List directory contents           |
| `ls -l`          | Detailed file listing             |
| `ls -a`          | Show hidden files                 |
| `ls -lh`         | Human-readable file sizes         |
| `cd <directory>` | Change directory                  |
| `cd ..`          | Move to parent directory          |
| `cd ~`           | Go to home directory              |
| `tree`           | Display directory structure       |

---

## Creating Files & Directories

| Command               | Purpose                   |
| --------------------- | ------------------------- |
| `touch file.txt`      | Create an empty file      |
| `mkdir folder`        | Create a new directory    |
| `mkdir -p dir/subdir` | Create nested directories |
| `mktemp`              | Create a temporary file   |

---

## Copying & Moving

| Command           | Purpose                        |
| ----------------- | ------------------------------ |
| `cp file1 file2`  | Copy a file                    |
| `cp -r dir1 dir2` | Copy a directory recursively   |
| `mv old new`      | Rename or move a file          |
| `mv file dir/`    | Move file to another directory |

---

## Deleting

| Command         | Purpose                        |
| --------------- | ------------------------------ |
| `rm file`       | Delete a file                  |
| `rm -r folder`  | Delete a directory recursively |
| `rm -rf folder` | Force delete directory         |
| `rmdir folder`  | Remove an empty directory      |

---

## Viewing File Contents

| Command           | Purpose                        |
| ----------------- | ------------------------------ |
| `cat file`        | Display entire file            |
| `less file`       | View file page by page         |
| `more file`       | View file one screen at a time |
| `head file`       | Display first 10 lines         |
| `tail file`       | Display last 10 lines          |
| `tail -f log.txt` | Monitor file in real time      |

---

## Searching Files

| Command                   | Purpose                           |
| ------------------------- | --------------------------------- |
| `find /path -name "file"` | Search by filename                |
| `find . -type f`          | Find all files                    |
| `find . -type d`          | Find all directories              |
| `locate filename`         | Locate a file quickly             |
| `which command`           | Show executable location          |
| `whereis command`         | Locate binary, source, and manual |

---

## File Information

| Command         | Purpose               |
| --------------- | --------------------- |
| `stat file`     | Display file metadata |
| `file filename` | Identify file type    |
| `du -sh folder` | Show directory size   |
| `df -h`         | Display disk usage    |
| `lsblk`         | List storage devices  |

---

## Permissions & Ownership

| Command            | Purpose                  |
| ------------------ | ------------------------ |
| `chmod 755 file`   | Change file permissions  |
| `chown user file`  | Change file owner        |
| `chgrp group file` | Change group ownership   |
| `umask`            | View default permissions |

---

## Links

| Command             | Purpose                |
| ------------------- | ---------------------- |
| `ln file link`      | Create a hard link     |
| `ln -s target link` | Create a symbolic link |

---

## Useful Utilities

| Command               | Purpose                            |
| --------------------- | ---------------------------------- |
| `wc file`             | Count lines, words, and characters |
| `basename /path/file` | Display filename only              |
| `dirname /path/file`  | Display directory path             |
| `realpath file`       | Show absolute file path            |
| `sync`                | Flush filesystem buffers to disk   |

---

## Important Directories

| Directory | Purpose                        |
| --------- | ------------------------------ |
| `/home`   | User home directories          |
| `/root`   | Root user's home directory     |
| `/etc`    | System configuration files     |
| `/var`    | Logs and variable data         |
| `/tmp`    | Temporary files                |
| `/usr`    | User applications and binaries |
| `/bin`    | Essential command binaries     |
| `/opt`    | Optional software packages     |

