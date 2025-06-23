# Network-Port-Scan
Cyber Security Internship - Task 1: Network Port Scanning

🔍 Local Network Port Scanning with Nmap
📋 Objective
This project demonstrates how to scan your local network to identify active devices, open ports, and potential security risks using Nmap and optional Wireshark analysis.

🛠️ Steps to Perform
1. Find Your Local Network Range
Open Command Prompt (Windows) or Terminal (Linux/macOS).

Run: ifconfig OR ipaddr
Note your IPv4 Address and Subnet Mask.
Calculate your network range (e.g., 192.168.1.0/24).

2. Run TCP SYN Scan with Nmap
Open Terminal/Command Prompt with admin privileges.

Run the following command: nmap -sS <your_network_range>
Example: nmap -sS 192.168.142.128/24


3. Note Down Discovered Hosts and Open Ports
Review the Nmap output.

Document: IP addresses of active devices.
Open ports and their associated services.

4. Optional: Analyze Traffic with Wireshark
Open Wireshark and select the appropriate network interface.
Start capturing packets before running Nmap.
Apply filter to view SYN packets: tcp.flags.syn==1 && tcp.flags.ack==0


5. Research Common Services on Open Ports
Identify what services run on discovered ports.

Examples:
Port 22 is used for SSH (Secure Shell), which provides remote shell access to devices. It is commonly used by system administrators to securely manage servers and devices over a network.
Port 80 is used for HTTP (Hypertext Transfer Protocol), which is the standard protocol for accessing websites and web servers in an unencrypted format.
Port 443 is used for HTTPS (Hypertext Transfer Protocol Secure), which provides secure, encrypted communication over the web. It ensures data transmitted between the client and server is protected.
Port 445 is used for SMB (Server Message Block), which is a protocol primarily used for Windows file and printer sharing over a network. It allows devices to share resources like files and printers.
Port 3389 is used for RDP (Remote Desktop Protocol), which allows users to remotely access and control Windows machines through a graphical interface.

7. Identify Potential Security Risks
Unnecessary open ports can be exploited.
Examples of risks:
SSH (22):Brute-force attacks.
Web Ports (80/443):Vulnerable applications.
SMB (445):EternalBlue/SMB exploits.
RDP (3389):Unauthorized remote access.

📚Requirements
 1. Nmap  
 2. Wireshark (optional)  

✅ Conclusion
Local network scanning helps identify vulnerabilities, providing an opportunity to strengthen network security before attackers exploit weaknesses.



⚠️ **Disclaimer**
This project is for **educational purposes** and intended for scanning your **own network only**. Unauthorized scanning of other networks is illegal.

