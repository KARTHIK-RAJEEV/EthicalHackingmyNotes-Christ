 1. BASIC LINUX COMMANDS
    
These are the foundational commands used to interact with the file system and manage files.

pwd — Print Working Directory
Shows your current location in the file system.
Example: /home/kali

ls — List Files and Folders
Lists the contents of a directory. Add -l for detailed list, -a to show hidden files.
Example: ls -la

cd <directory> — Change Directory
Moves into another folder.
Example: cd Desktop

mkdir <foldername> — Make Directory
Creates a new folder.
Example: mkdir hacking_tools

rm <file> — Remove File
Deletes a file. Use rm -r <folder> to remove directories. Be cautious with rm -rf.

cp <source> <destination> — Copy Files/Folders
Makes a duplicate of a file or folder.
Example: cp file.txt /home/kali/Desktop

mv <old> <new> — Move/Rename File
Moves a file to a new location or renames it.

touch <filename> — Create File
Creates an empty file.

cat <file> — View File Content
Prints the content of a file in the terminal.

clear — Clear Terminal
Clears all previous output on the terminal screen.


🔐 2. USER AND PERMISSION COMMANDS


Useful when managing users or securing files.

whoami — Current User
Displays the username of the current logged-in user.

sudo <command> — Run as Superuser
Executes a command with administrative privileges.

chmod — Change File Permissions
Controls who can read/write/execute a file.
Example: chmod +x script.sh makes it executable.

chown — Change File Ownership
Changes who owns a file.
Example: chown kali:kali file.txt

adduser — Add New User
Creates a new user on the system.

passwd — Change Password
Used to change the password for a user.

🌐 3. NETWORKING COMMANDS

Essential for scanning, analyzing, and attacking networks.

ifconfig — Show Network Interfaces
Displays IP addresses and status of network devices.
(Use ip a in newer versions of Linux.)

iwconfig — Wireless Interface Info
Shows wireless-specific details (SSID, mode, etc.).

ping <host> — Check Connectivity
Sends ICMP packets to test network connection.

netstat -tuln — Show Open Ports
Lists all open ports and their listening services.

nmap <ip> — Network Mapper
Scans a host or range of IPs to discover open ports, services, OS, and vulnerabilities.

tcpdump — Packet Sniffer
Captures and displays packets going through the network interface.

traceroute <host> — Trace Path
Shows each hop between your system and the destination.

curl / wget — Download via Terminal
Used to download content from a URL.

🧰 4. KALI LINUX PENETRATION TESTING TOOLS

Pre-installed tools specifically for ethical hacking.

msfconsole — Metasploit Framework
A powerful tool for exploitation and post-exploitation.
Run it to launch the Metasploit console.

hydra — Brute Force Login Attacks
Performs dictionary attacks on login systems like SSH, FTP, etc.

airmon-ng — Enable Monitor Mode
Prepares wireless interface for packet capture (used with aircrack-ng).

aircrack-ng — WiFi Cracking Tool
Crack WEP/WPA keys after capturing handshakes.

sqlmap — SQL Injection Automation
Automates detection and exploitation of SQL injection flaws.

burpsuite — Web Application Tester
GUI-based proxy to test and modify traffic between browser and server.

john — Password Cracker
Cracks password hashes using dictionary or brute-force attacks.

📦 5. PACKAGE MANAGEMENT WITH APT

APT (Advanced Package Tool) is used to install, update, and remove tools in Kali Linux.

apt update — Update Package List
Fetches the latest available versions of packages.

apt upgrade — Upgrade Installed Packages

apt install <tool> — Install a New Tool
Example: apt install nmap

apt remove <tool> — Remove a Tool

dpkg -i <file.deb> — Install a .deb File
Useful for installing manually downloaded packages.

🔍 6. SYSTEM MONITORING & INFORMATION

Monitor system performance and retrieve information.

df -h — Disk Space Usage
Shows space used and free on mounted drives.

du -sh <folder> — Folder Size

top or htop — Process Monitor
htop is more user-friendly with colors and interactive interface.

uname -a — System Info
Displays kernel and architecture details.

ps aux — Running Processes

uptime — System Running Time

dmesg — Boot and Kernel Logs

🧪 7. COMMON PENTESTING PHASES & TOOLS
Understanding what tools are used in different phases of a security assessment.

Phase	Tools
Reconnaissance	nmap, dnsenum, whois, theHarvester
Scanning	nmap, nikto, wpscan
Gaining Access	msfconsole, hydra, sqlmap, exploitdb
Maintaining Access	Metasploit backdoors, netcat
Covering Tracks	clearev, history -c, log cleaning
