# cybersec-internship-task5
# Cybersecurity Internship - Task 5 (Wireshark Packet Analysis on Kali Linux)

**Task:** Capture and analyze live network traffic using Wireshark.  

## 🎯 Objective
Learn to capture live packets on Kali Linux, filter them, and understand how network protocols work in real time.

---

## 🛠️ Steps Performed

### 1. Install Wireshark
```bash
sudo apt update
sudo apt install wireshark -y
```
2. Start Wireshark

Launched Wireshark GUI:
```
wireshark &

```
Selected the active interface (wlan0).

Clicked Start Capturing Packets.
3. Generate Traffic

I ran a ping command to Google to generate ICMP traffic:
```
ping -c 5 google.com
```
Output:
```
PING google.com (2404:6800:4009:809::200e) 56 data bytes
64 bytes from pnbomb-bo-in-x0e.1e100.net (2404:6800:4009:809::200e): icmp_seq=1 ttl=116 time=211 ms
64 bytes from pnbomb-bo-in-x0e.1e100.net (2404:6800:4009:809::200e): icmp_seq=2 ttl=116 time=223 ms
64 bytes from pnbomb-bo-in-x0e.1e100.net (2404:6800:4009:809::200e): icmp_seq=3 ttl=116 time=245 ms
64 bytes from pnbomb-bo-in-x0e.1e100.net (2404:6800:4009:809::200e): icmp_seq=4 ttl=116 time=267 ms
64 bytes from pnbomb-bo-in-x0e.1e100.net (2404:6800:4009:809::200e): icmp_seq=5 ttl=116 time=289 ms

--- google.com ping statistics ---
5 packets transmitted, 5 received, 0% packet loss, time 4008ms
rtt min/avg/max/mdev = 211.386/246.739/288.526/28.211 ms
```

4. Stop Capture

After ~1 minute, clicked the Stop button in Wireshark.

Saved the capture as capture2.pcap
5. Filter Packets

Used Wireshark filters:

dns → DNS queries.

tcp → TCP connections.

icmp → ICMP ping packets
🔍 Protocols Identified

DNS (Port 53): Domain resolution.

TCP (Port 80/443): Web browsing traffic.

ICMP: Ping packets to Google.
📊 Outcome

Successfully generated and captured live traffic on Kali Linux.

Identified DNS, TCP, and ICMP protocols.

Gained practical experience in analyzing packets.

📎 Deliverables

capture.pcap (Wireshark export).

report.md (protocol analysis).

Screenshots in screenshots/ folder.
