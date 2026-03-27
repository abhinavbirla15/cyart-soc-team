# Notes – SOC Operations

## 1. Alert Priority Levels

### What is Alert Priority?
SOC analysts receive many alerts daily. Priority helps decide which alerts to investigate first.

### Priority Levels

- Critical → Immediate action (e.g., ransomware, data theft)
- High → Serious threat (e.g., admin access, malware)
- Medium → Suspicious activity (e.g., brute-force attempts)
- Low → Minor activity (e.g., single failed login)

### Factors Affecting Priority

1. Asset Criticality  
   - Production server → High priority  
   - Test system → Low priority  

2. CVSS Score  
   - 9.0–10 → Critical  
   - 7.0–8.9 → High  
   - 4.0–6.9 → Medium  
   - 0–3.9 → Low  

3. Business Impact  
   - Even low vulnerability can be high priority if it affects important systems  

---

## 2. Incident Classification

### What is Incident Classification?
Grouping incidents based on type to understand and respond properly.

### Types of Incidents

- Malware  
- Phishing  
- Brute-force attacks  
- DDoS  
- Insider threats  
- Data exfiltration  

### Framework Used

MITRE ATT&CK:

- T1566 → Phishing  
- T1110 → Brute-force  
- T1190 → Exploit  

### Metadata

Each incident must include:
- Source IP  
- Timestamp  
- Target system  
- Indicators of Compromise (IOCs)  

---

## 3. Incident Response

### Lifecycle

1. Preparation  
2. Identification  
3. Containment  
4. Eradication  
5. Recovery  
6. Lessons Learned  

### Key Actions

- Isolate affected system  
- Collect logs  
- Document everything  
- Communicate with team  

---

## 4. Alert Management

Created alert table with:

- Alert ID  
- Type  
- Priority  
- MITRE Mapping  

Example:
- Phishing → High → T1566  
- Port Scan → Low → T1046  

---

## 5. Alert Triage

Analyzed alerts using:

- Source IP  
- Behavior  
- Threat intelligence tools  

Tools used:
- VirusTotal  
- AlienVault OTX  

---

## 6. Evidence Preservation

### Why Important?

- Needed for investigation  
- Maintains integrity  

### Hashing

Used SHA256:

sha256sum file.txt

This ensures file integrity.

---

## 7. Capstone Project

### Steps

1. Simulated attack using Metasploit  
2. Detected activity  
3. Performed triage  
4. Responded (blocked attacker)  
5. Documented incident  

---

## Key Learning

- Prioritization is important to handle alerts efficiently  
- Classification improves clarity  
- Incident response must follow proper steps  
- Documentation is critical in SOC operations  
