
---

### ✅ report.md
```markdown
# Wireshark Packet Analysis Report (Kali Linux)

## 1. Overview
This report summarizes the analysis of a packet capture performed on Kali Linux using Wireshark.  
Traffic was generated using:
- `ping -c 5 google.com` (ICMP packets)  
- Web browsing (DNS, TCP/HTTP/HTTPS packets)  

---

## 2. Protocols Observed

### 🔹 ICMP
- **Purpose:** Internet Control Message Protocol used for diagnostics.  
- **Observation:** Echo request/reply packets exchanged with `google.com`.  
- **Risk:** ICMP can be abused in attacks like ping floods (DoS).  

---

### 🔹 DNS
- **Purpose:** Resolves domain names into IP addresses.  
- **Observation:** Queries made for domain lookups when browsing websites.  
- **Risk:** DNS poisoning or tunneling can be exploited by attackers.  

---

### 🔹 TCP
- **Purpose:** Provides reliable, connection-oriented communication.  
- **Observation:** TCP 3-way handshake and session traffic captured.  
- **Risk:** Open TCP ports may expose services to attacks.  

---

### 🔹 HTTP/HTTPS
- **Purpose:** Application layer protocol for web traffic.  
- **Observation:**  
  - HTTP: Possible unencrypted traffic.  
  - HTTPS (TLS): Encrypted communication for security.  
- **Risk:** HTTP traffic is vulnerable to sniffing; HTTPS is more secure but still subject to SSL/TLS attacks if misconfigured.  

---

## 3. Security Insights
- ICMP should be rate-limited to avoid abuse.  
- DNS traffic should be monitored for anomalies (tunneling).  
- Only necessary TCP/UDP ports should be left open.  
- HTTPS should always be used instead of HTTP to prevent credential theft.  

---

## 4. Conclusion
Wireshark successfully captured ICMP, DNS, TCP, and HTTP/HTTPS traffic.  
This exercise demonstrated how to filter and analyze packets, providing insights into network behavior and potential risks.
