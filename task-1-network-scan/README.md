# Task 1: Network Port Scanning using Nmap

## 📌 Objective

To perform network scanning on a local network and identify open ports, running services, and potential security risks.

---

## 🛠️ Tools Used

* Nmap (Network Scanner)
* Wireshark (Packet Analysis - Optional)

---

## 🌐 Target Network

192.168.139.0/24

---

## ⚙️ Command Used

```bash
nmap -sS 192.168.139.0/24
```

---

## 📊 Scan Results

* Total Active Hosts Found: 3

* Open Port Detected:

  * **192.168.139.2 → Port 53 (DNS)**

* Other Hosts:

  * Ports are filtered (likely protected by firewall)

---

## 🔎 Service Analysis

### 🔓 Port 53 – DNS (Domain Name System)

DNS is used to translate domain names (e.g., google.com) into IP addresses.

---

## ⚠️ Security Risks Identified

* **DNS Amplification Attack**
  Attackers can exploit DNS servers for DDoS attacks.

* **DNS Spoofing / Poisoning**
  Fake responses can redirect users to malicious websites.

* **Information Disclosure**
  DNS queries can reveal internal network structure.

* **Open Port Exposure**
  Any open port increases attack surface.

---

## 🔐 Mitigation / Security Measures

* Close unused ports
* Configure firewall rules
* Use secure DNS configurations
* Apply regular updates and patches
* Monitor network traffic

---

## 📁 Output Files

* Scan results saved in: `result.txt`

---

## 🧠 Conclusion

This task provided hands-on experience in network reconnaissance using Nmap. It helped in understanding how open ports expose services and how they can be potential entry points for attackers.

---

# 🎯 Interview Questions & Answers

## 1. What is an open port?

An open port is a communication endpoint that is actively accepting connections and running a service.

---

## 2. How does Nmap perform a TCP SYN scan?

Nmap sends a SYN packet to the target port:

* SYN-ACK response → Port is open
* RST response → Port is closed

This is called a half-open scan because the connection is not fully established.

---

## 3. What risks are associated with open ports?

* Unauthorized access
* Brute-force attacks
* Exploitation of vulnerable services
* Data leakage

---

## 4. Explain the difference between TCP and UDP scanning.

**TCP Scanning:**

* Connection-oriented
* Reliable
* Easier to detect

**UDP Scanning:**

* Connectionless
* Faster but less reliable
* Harder to detect

---

## 5. How can open ports be secured?

* Disable unused ports
* Use firewalls
* Implement authentication
* Keep services updated
* Use IDS/IPS systems

---

## 6. What is a firewall's role regarding ports?

A firewall monitors and controls incoming and outgoing traffic. It allows or blocks ports based on security rules.

---

## 7. What is a port scan and why do attackers perform it?

Port scanning is the process of identifying open ports and services on a system. Attackers use it to find vulnerabilities and entry points.

---

## 8. How does Wireshark complement port scanning?

Wireshark captures and analyzes network packets. It helps understand how scanning works at the packet level by observing SYN, SYN-ACK, and RST responses.

---

