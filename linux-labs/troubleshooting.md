# Linux Troubleshooting Lab

## Objective
Practice basic Linux administration and troubleshooting commands used in cloud support.

## System Information
- `hostname` — displays the system hostname.
- `uptime` — shows system uptime and load averages.
- `df -h` — checks filesystem disk usage.
- `free -h` — displays memory usage.

## Processes and Services
- `ps aux` — lists running processes.
- `top` — monitors processes and resource usage.
- `systemctl status <service>` — checks a service's status on systemd-based Linux systems.

## Network Troubleshooting
- `ip addr` — displays network interfaces and IP addresses.
- `ip route` — displays routing information.
- `ss -tuln` — lists listening TCP and UDP sockets.
- `curl -I https://example.com` — checks HTTP response headers from a website.

## Log Analysis
- `journalctl -p err -b` — shows error-priority journal entries from the current boot.
- `tail -n 50 /var/log/syslog` — displays recent syslog entries on systems that use this file.

## Learning Notes
These commands are documented for practice. Record actual command outputs and troubleshooting results after running the labs on a Linux system.

## Lab 02: TCP and HTTPS Connectivity

### Objective
Test TCP connectivity and HTTPS responses from a Windows client.

### Commands
- `Test-NetConnection amazon.com -Port 443`
- `curl.exe -I --max-time 10 https://amazon.com`

### Results
- TCP port 443: Successful (TcpTestSucceeded: True)
- HTTPS response: HTTP 301 Moved Permanently

### Analysis
The TCP connection to port 443 succeeded.
The server returned an HTTP redirect, indicating
that it responded to the HTTPS request.

### Environment
Windows 11 local networking lab. No AWS resources were created.
## Lab 03: DNS Record Investigation

### Objective
Investigate DNS records using Windows command-line tools.

### Commands
- `nslookup -type=A amazon.com`
- `nslookup -type=MX gmail.com`
- `ipconfig /all`

### Results
- A record query: Successful
- MX record query: Successful
- Configured Wi-Fi DNS server: DNS servers configured on the Wi-Fi adapter

### Analysis
DNS queries returned records successfully, confirming
that hostname resolution worked during testing.

### Environment
Windows 11 local networking lab. No AWS resources were created.
