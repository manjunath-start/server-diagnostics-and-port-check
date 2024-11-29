# Server Diagnostics and Port Check

This repository contains the results and steps for diagnosing server connectivity issues, checking system resource usage, and verifying port availability for an application. 

## Tasks Covered

### Task 1: Diagnostics
1. **Get the IP address of a domain (`guvi.in`)**:
   - Command used: `nslookup guvi.in` or `dig guvi.in +short`

2. **Check CPU and memory usage**:
   - CPU usage: `top` or `mpstat`
   - Memory usage: `free -h`

3. **Test connectivity between two nodes**:
   - Command used: `ping -c 4 <destination_ip_or_hostname>`
   - Alternative for specific ports: `telnet <destination_ip_or_hostname> <port_number>`

### Task 2: Port Availability Check
1. **Verify if port `9000` is open on `guvi.com`**:
   - Command used: `nc -zv guvi.com 9000`

2. **Debugging steps if the application is inaccessible**:
   - Check if the application is running and listening:
     ```bash
     netstat -tuln | grep 9000
     ```
   - Verify firewall rules:
     ```bash
     sudo ufw status
     sudo ufw allow 9000/tcp
     ```

### Execution Environment
- Tools used: Shell (AWS CLI, Gitbash, WSL, VirtualBox)
- OS: Linux-based environments (Ubuntu, etc.)

## Repository Contents
1. **Commands and Outputs**:
   - Screenshots of command outputs for each task.
   - Commands are labeled and include results.

2. **Files**:
   - `commands.txt`: A text file listing all the commands used.
   - `screenshots/`: A directory containing output screenshots.

## How to Run
- Open the terminal in a Linux-based shell.
- Run the commands mentioned in `commands.txt` to replicate the results.

## Results
All tasks were successfully executed:
- IP address retrieved for `guvi.in`.
- CPU and memory usage verified.
- Connectivity between two nodes tested.
- Port availability on `guvi.com:9000` verified.

## Repository URL
To be submitted as per portal requirements.
