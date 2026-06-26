# Common Linux Commands Cheat Sheet

This cheat sheet contains frequently used Linux commands for quick reference. Use it as a handy guide while working on Linux systems.

---

## System Information

| Command    | Purpose                               |
| ---------- | ------------------------------------- |
| `pwd`      | Print current working directory       |
| `whoami`   | Display current logged-in user        |
| `hostname` | Show system hostname                  |
| `uname -a` | Display kernel and system information |
| `date`     | Show current date and time            |
| `uptime`   | Display system uptime                 |
| `history`  | Show previously executed commands     |
| `clear`    | Clear the terminal screen             |

---

## Help Commands

| Command             | Purpose                                 |
| ------------------- | --------------------------------------- |
| `man <command>`     | Open manual page                        |
| `<command> --help`  | Display command usage                   |
| `info <command>`    | View GNU documentation                  |
| `which <command>`   | Show command location                   |
| `whereis <command>` | Locate binary, source, and manual pages |

---

## User Information

| Command  | Purpose                             |
| -------- | ----------------------------------- |
| `id`     | Display user and group IDs          |
| `groups` | Show user groups                    |
| `who`    | Display logged-in users             |
| `w`      | Show logged-in users and activities |

---

## Permissions

| Command | Purpose                            |
| ------- | ---------------------------------- |
| `chmod` | Change file permissions            |
| `chown` | Change file owner                  |
| `chgrp` | Change group ownership             |
| `umask` | Display or set default permissions |

---

## Package Management (APT)

| Command                      | Purpose                    |
| ---------------------------- | -------------------------- |
| `sudo apt update`            | Update package list        |
| `sudo apt upgrade`           | Upgrade installed packages |
| `sudo apt install <package>` | Install a package          |
| `sudo apt remove <package>`  | Remove a package           |
| `sudo apt autoremove`        | Remove unused packages     |

---

## Process Management

| Command          | Purpose                       |
| ---------------- | ----------------------------- |
| `ps`             | View running processes        |
| `ps aux`         | Display all running processes |
| `top`            | Monitor system processes      |
| `kill <PID>`     | Terminate a process           |
| `killall <name>` | Kill all processes by name    |

---

## Networking

| Command    | Purpose                   |
| ---------- | ------------------------- |
| `ip a`     | Display IP configuration  |
| `ping`     | Test network connectivity |
| `ss -tuln` | Show listening ports      |
| `curl`     | Transfer data from URLs   |
| `wget`     | Download files            |

---

## File Compression

| Command    | Purpose             |
| ---------- | ------------------- |
| `tar -cvf` | Create archive      |
| `tar -xvf` | Extract archive     |
| `gzip`     | Compress file       |
| `gunzip`   | Decompress file     |
| `zip`      | Create ZIP archive  |
| `unzip`    | Extract ZIP archive |

---

## Monitoring

| Command   | Purpose                           |
| --------- | --------------------------------- |
| `free -h` | Display memory usage              |
| `df -h`   | Show disk usage                   |
| `du -sh`  | Show directory size               |
| `vmstat`  | Display virtual memory statistics |
| `iostat`  | Display CPU and disk statistics   |

---

## Useful Keyboard Shortcuts

| Shortcut   | Purpose                  |
| ---------- | ------------------------ |
| `Ctrl + C` | Stop current process     |
| `Ctrl + Z` | Suspend process          |
| `Ctrl + D` | Logout / End input       |
| `Ctrl + L` | Clear terminal           |
| `Ctrl + R` | Search command history   |
| `Tab`      | Auto-complete commands   |
| `↑ / ↓`    | Navigate command history |

