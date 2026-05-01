# 🌐 Network Traffic Analysis & Packet Inspection

## 🔹 Overview
This project documents my learning of network traffic analysis, packet inspection, and monitoring techniques used in cybersecurity to detect and investigate suspicious activity.

---

## 🔹 Key Concepts Learned

### 1. Network Traffic Flow
- Understanding how data moves across a network  
- Importance of monitoring traffic for unusual patterns  
- Helps detect anomalies and potential security threats  

---

### 2. Network Monitoring
- Continuous observation of network activity  
- Maintains awareness of system behavior  
- Helps identify unauthorized access or abnormal traffic  

---

### 3. Data Exfiltration Attacks
- Unauthorized transfer of data from a system  
- Often hidden within normal network traffic  
- Requires monitoring tools to detect  

---

### 4. Packets & Packet Capture
- Data is transmitted in small units called **packets**  
- Packet capture allows analysis of:
  - Source and destination  
  - Protocol used  
  - Payload data  

---

### 5. Packet Inspection
- Examining packet contents to understand communication  
- Helps detect malicious activity  
- Includes analyzing:
  - Headers  
  - Payload  

---

### 6. Packet Header Analysis
Key fields analyzed:
- Source IP  
- Destination IP  
- Protocol (TCP/UDP)  
- Port numbers  
- Flags (SYN, ACK, FIN)  

---

### 7. Network Protocols
- TCP (Transmission Control Protocol)  
- UDP (User Datagram Protocol)  
- HTTP (Web communication)  
- DNS (Domain Name System)  

---

## 🔹 Tools Used

### tcpdump
A command-line tool used for capturing and analyzing network traffic.

---

## 🔹 Practical Commands Used

### View network interfaces
```bash
sudo ifconfig

List available capture interfaces
sudo tcpdump -D
Capture live packets
sudo tcpdump -i eth0 -v -c5
Capture and save packets to file
sudo tcpdump -i eth0 -nn -c9 port 80 -w capture.pcap
Read captured packets
sudo tcpdump -nn -r capture.pcap -v
View packet data in hex and ASCII
sudo tcpdump -nn -r capture.pcap -X

🔹 Packet Analysis Example
TCP 3-Way Handshake
SYN → Request connection
SYN-ACK → Acknowledgment
ACK → Connection established

HTTP Request Observed
GET / HTTP/1.1
Host: opensource.google.com
User-Agent: curl/7.74.0

HTTP Response
Status: 301 Moved Permanently
Redirects to HTTPS version of the site

🔹 Key Observations
Successful TCP connection established
HTTP request sent using curl
Server responded with redirect (HTTP → HTTPS)
Packet headers revealed communication details
Traffic captured and stored in .pcap file

🔹 Learning Outcomes
Understanding of network traffic flow
Ability to capture and analyze packets using tcpdump
Knowledge of packet structure and headers
Identification of HTTP communication patterns
Awareness of data exfiltration risks
Hands-on experience with packet inspection

🔹 Conclusion

This project improved my ability to analyze network communications and understand how cybersecurity professionals monitor and investigate network activity in real-world environments.
