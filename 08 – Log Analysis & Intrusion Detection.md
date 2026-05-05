# 🛡️ Log Analysis & Intrusion Detection

## Overview
This section documents my understanding of log analysis, security monitoring, and intrusion detection systems. It also includes hands-on experience using Suricata for detecting network activity and analyzing logs.

---

## Importance of Logs
Logs are critical in cybersecurity because they:
- Record system and network activities
- Help detect suspicious behavior
- Support incident investigation and response
- Provide evidence during security incidents

---

## Log Analysis
Log analysis involves examining log data to:
- Identify anomalies
- Detect threats and attacks
- Understand system behavior

---

## Types of Logs
- System logs
- Network logs
- Application logs
- Security logs

---

## Log Management
### Best Practices:
- Centralized log collection
- Secure log storage
- Regular monitoring and review
- Log retention policies

### Key Concepts:
- Overlogging: collecting excessive unnecessary logs
- Log retention: how long logs are stored
- Log protection: preventing unauthorized access or modification

---

## Log Formats
Common log formats include:

### 1. JSON (JavaScript Object Notation)
- Uses:
  - Curly brackets `{ }`
  - Double quotes `"`
- Structured and easy to parse
- Used in tools like Suricata (EVE JSON)

### 2. Syslog
- Standard format for system logging
- Contains:
  - Header
  - Structured data
  - Message

### 3. XML (eXtensible Markup Language)
- Uses tags `< >`
- Structured but more verbose

### 4. CSV (Comma Separated Values)
- Uses commas to separate values
- Simple and widely used

### 5. CEF (Common Event Format)
- Standardized format for security tools

---

## Log Components
- Timestamp
- Source and destination IP
- Protocol
- Service
- Message content

---

## Security Monitoring & Detection
Security monitoring involves:
- Observing system activity
- Detecting threats in real-time
- Responding to suspicious behavior

---

## Detection Techniques

### 1. Signature-Based Detection
- Detects known attack patterns

#### Advantages:
- Accurate for known threats

#### Disadvantages:
- Cannot detect new (unknown) attacks

---

### 2. Anomaly-Based Detection
- Detects unusual behavior

#### Advantages:
- Can detect unknown threats

#### Disadvantages:
- Higher false positives

---

## Intrusion Detection Systems (IDS)

### Types:
- Network-based IDS (NIDS)
- Host-based IDS (HIDS)

---

## Suricata (Practical Lab)

### Custom Rule

alert http $HOME_NET any -> $EXTERNAL_NET any (msg:"GET on wire"; flow:established,to_server; content:"GET"; http_method; sid:12345; rev:3;)

### Running Suricata
sudo suricata -r sample.pcap -S custom.rules -k none

---

## Generated Logs

### Log Files:
- eve.json
- fast.log
- stats.log
- suricata.log

---

## fast.log Output (Alerts)

[] [1:12345:3] GET on wire [] {TCP} 172.21.224.2 -> 142.250.1.139:80

---

## EVE JSON Log Analysis

Example:

---

## EVE JSON Log Analysis

Example:
{
"timestamp": "2022-11-23T12:38:34.624866+0000",
"event_type": "alert",
"src_ip": "172.21.224.2",
"dest_ip": "142.250.1.139",
"proto": "TCP",
"alert": {
"signature": "GET on wire",
"severity": 3
},
"http": {
"hostname": "opensource.google.com",
"http_method": "GET",
"status": 301
}
}

---

## Log Analysis Using jq

### Pretty Print Logs
jq . eve.json

### Extract Specific Fields
jq -c "[.timestamp,.flow_id,.alert.signature,.proto,.dest_ip]" eve.json

### Filter Specific Events
jq 'select(.flow_id==VALUE)' eve.json

---

## SIEM & Log Querying
Tools used for log analysis:
- SIEM platforms
- Splunk
- Google SecOps
- Wazuh

### Capabilities:
- Event searching
- Log correlation
- Threat detection

---

## Key Concepts Learned
- Log collection and management
- Log formats (JSON, Syslog, XML, CSV)
- Intrusion detection systems (NIDS, HIDS)
- Signature vs anomaly detection
- Suricata rule creation and execution
- Network telemetry and monitoring
- Querying logs using jq and SIEM tools

---

## Learning Outcomes
- Developed ability to analyze logs for security insights
- Understood detection techniques and IDS systems
- Gained hands-on experience with Suricata
- Learned how to extract and filter log data
- Improved understanding of real-world security monitoring

---

## Conclusion
This section demonstrates my ability to work with logs, detect threats, and analyze network activity using industry-relevant tools and techniques.

---

📌 This project is part of my cybersecurity portfolio and hands-on learning journey.
