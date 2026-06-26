# Linux Networking Commands (In detail) 

This cheat sheet contains commonly used Linux networking commands for troubleshooting, network analysis, and basic cybersecurity tasks.

---

## Network Configuration

| Command        | Purpose                                |
| -------------- | -------------------------------------- |
| `ip a`         | Display IP addresses of all interfaces |
| `ip addr show` | Show detailed IP configuration         |
| `ip link show` | Display network interfaces             |
| `ip route`     | Show routing table                     |
| `hostname -I`  | Display local IP address               |

---

## Connectivity Testing

| Command             | Purpose                                    |
| ------------------- | ------------------------------------------ |
| `ping <host>`       | Test connectivity to a host                |
| `traceroute <host>` | Display the route packets take             |
| `tracepath <host>`  | Trace network path without root privileges |
| `mtr <host>`        | Continuous network diagnostics             |
| `arp -a`            | Display ARP cache                          |

---

## DNS Commands

| Command                | Purpose                        |
| ---------------------- | ------------------------------ |
| `nslookup <domain>`    | Query DNS information          |
| `dig <domain>`         | Retrieve detailed DNS records  |
| `host <domain>`        | Resolve hostname to IP address |
| `cat /etc/resolv.conf` | View DNS server configuration  |

---

## Port and Connection Monitoring

| Command         | Purpose                                        |
| --------------- | ---------------------------------------------- |
| `ss -tuln`      | Display listening TCP/UDP ports                |
| `ss -tunap`     | Show listening ports with associated processes |
| `netstat -tuln` | List active ports (legacy command)             |
| `lsof -i`       | Display processes using network connections    |

---

## Remote Access

| Command                    | Purpose                      |
| -------------------------- | ---------------------------- |
| `ssh user@host`            | Connect to a remote system   |
| `scp file user@host:/path` | Securely copy files          |
| `sftp user@host`           | Secure file transfer session |

---

## Data Transfer

| Command      | Purpose                     |
| ------------ | --------------------------- |
| `curl <URL>` | Transfer data from a URL    |
| `wget <URL>` | Download files from the web |

---

## Packet Capture and Analysis

| Command             | Purpose                                   |
| ------------------- | ----------------------------------------- |
| `tcpdump -i any`    | Capture packets from all interfaces       |
| `tcpdump -i eth0`   | Capture packets from a specific interface |
| `tcpdump port 80`   | Capture HTTP traffic                      |
| `tcpdump host <IP>` | Capture traffic for a specific host       |

---

## Network Statistics

| Command               | Purpose                                |
| --------------------- | -------------------------------------- |
| `ifconfig`            | Display interface information (legacy) |
| `iwconfig`            | Display wireless interface information |
| `ethtool eth0`        | Display Ethernet interface details     |
| `nmcli device status` | Show NetworkManager device status      |

---

## Useful Cybersecurity Commands

| Command             | Purpose                              |
| ------------------- | ------------------------------------ |
| `nmap <IP>`         | Scan host for open ports             |
| `nmap -sV <IP>`     | Detect running services and versions |
| `nmap -O <IP>`      | Detect operating system              |
| `netcat -lvnp 4444` | Start a TCP listener                 |
| `netcat <IP> 4444`  | Connect to a TCP listener            |

---

## Firewall

| Command             | Purpose                 |
| ------------------- | ----------------------- |
| `sudo ufw status`   | Display firewall status |
| `sudo ufw enable`   | Enable UFW firewall     |
| `sudo ufw allow 22` | Allow SSH traffic       |
| `sudo ufw deny 80`  | Block HTTP traffic      |

---

## Useful Files

| File                      | Purpose                                                |
| ------------------------- | ------------------------------------------------------ |
| `/etc/hosts`              | Local hostname resolution                              |
| `/etc/resolv.conf`        | DNS configuration                                      |
| `/etc/network/interfaces` | Network interface configuration (Debian-based systems) |
| `/etc/hostname`           | System hostname                                        |
| `/etc/hosts.allow`        | TCP Wrapper allow rules                                |
| `/etc/hosts.deny`         | TCP Wrapper deny rules                                 |

