# google-cybersecurity-certificate-Network-Traffic-Analysis-assessment-
Analyzing tcpdump network logs to diagnose DNS failures and translating packet data into an incident report.
## Project Overview
This project demonstrates the ability to analyze raw network traffic logs to diagnose service outages and translate technical findings into an actionable incident report. Originally completed as part of the Google Cybersecurity Certificate, this exercise bridges the gap between technical packet inspection and stakeholder communication.

## Scenario
Several customers reported an inability to access a client website (`www.yummyrecipesforme.com`), receiving a "destination port unreachable" error. The objective was to utilize command-line network analysis tools to inspect the traffic, identify the protocol failures, and document the root cause for IT leadership.

## Tools & Skills Utilized
* **Network Analysis:** `tcpdump`, Packet Sniffing, Log Analysis
* **Protocol Inspection:** UDP, ICMP (Type 3, Code 3 Messages), DNS (Port 53)
* **Threat Identification:** Denial of Service (DoS) recognition, Firewall Misconfiguration 
* **Governance & Reporting:** stakeholder communication, structured incident reporting

## Key Findings
* **Log Analysis:** Examined `tcpdump` logs detailing traffic between the client IP (192.51.100.15) and the DNS server (203.0.113.2).
* **Protocol Failure:** Identified that the DNS server was actively online but returning an ICMP Destination Unreachable (Port Unreachable) error specifically for `udp port 53`.
* **Root Cause Hypothesis:** Concluded that the DNS service failure was likely caused by either a misconfigured firewall blocking port 53 or an active DoS attack overwhelming the service.

## Documentation
* [Read the full Incident Report (PDF)](network-traffic-analysis-report)
