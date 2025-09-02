# MAC-Flooding-using-macof

cybersecurity, ethical-hacking, macof, dsniff, networking, lab, penetration-testing, switch-security









\## 📖 Overview

This lab demonstrates how to perform a \*\*MAC Flooding attack\*\* using the `macof` tool from the `dsniff` collection.  

MAC flooding is a technique used by attackers to compromise the security of network switches by forcing them into a "fail-open" state, enabling traffic sniffing.



---



\## 🧪 Lab Scenario

Attackers use \*\*MAC Flooding\*\* to overload the switch’s CAM (Content Addressable Memory) table with fake MAC addresses.  

When the CAM table is full, the switch behaves like a hub, broadcasting traffic to all ports. An attacker can then place their network interface card (NIC) in \*\*promiscuous mode\*\* to capture and analyze this traffic.



---



\## 🎯 Lab Objectives

\- Understand how MAC Flooding works.

\- Use `macof` to generate fake MAC and IP addresses.

\- Observe how a switch reacts when its CAM table is overwhelmed.

\- Highlight the security risks of improper switch configurations.



---



\## 🛠️ Tools Used

\- \*\*Operating System:\*\* Linux  

\- \*\*Tool:\*\* \[macof](https://linux.die.net/man/8/macof) (part of the `dsniff` collection)



---



\## 📚 Steps Performed

1\. Verified network connectivity between devices in the lab environment.

2\. Launched the `macof` tool to generate large volumes of random MAC and IP addresses.  

&nbsp;  ```bash

&nbsp;  macof -i eth0



-i eth0 specifies the network interface.



By default, macof sends ~131,000 forged MAC entries per minute.



Observed how the switch’s CAM table was flooded and forced into fail-open mode.



Enabled promiscuous mode on the attacker’s NIC to capture broadcast traffic.



ifconfig eth0 promisc



Used a packet-sniffing tool Wireshark to analyze captured traffic.



⚠️ Security Implications



MAC Flooding attacks allow adversaries to intercept sensitive data on the network.



Organizations should implement countermeasures like:



Port security (limit the number of MAC addresses per port).



Dynamic ARP inspection (DAI).



802.1X authentication.



Using dedicated VLANs for sensitive traffic.



📌 Key Takeaways



A full CAM table forces switches into hub-like behavior, exposing traffic to attackers.



Tools like macof demonstrate why switch hardening is critical in network security.



Understanding offensive techniques helps defenders build stronger protection strategies.



📷 Demo



https://github.com/rlinemavuyangwa/MAC-Flooding-using-macof/raw/refs/heads/main/MAC%20Flooding%20Demo.mp4

