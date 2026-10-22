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
Compare DNS resolution, TCP connectivity, and HTTP response results to narrow down possible connectivity issues.

### Environment
Windows 11 local networking lab. No AWS resources were created.
