
# Sprint-4-Anna-Francisco
Sprint 4 Wireshark
# Cyber Range Team Capstone Project Summary - Sprint 4 Anna & Fransico


[![SPRINT 4](https://user-images.githubusercontent.com/119987218/239769865-7e224571-cca0-42bf-befa-dc852d73bebf.png)](https://github.com/cybertrainingrange/Sprint-4-Anna-Francisco#readme) 



# Documentation: Interpreting Live Traffic Analysis with Wireshark

Introduction

Another technique for assessing the security of a host is to analyze traffic flowing into and out of the host. A popular tool for analysis of network traffic is Wireshark. Wireshark is free to use and runs on a variety of operating systems. Wireshark captures and records packets being transmitted and received from selected network interfaces of a host. You can then analyze the captured traffic by filtering and inspecting packets using the graphical user interface. To get the most benefit from this type of security analysis, you should understand the communication protocols and what type of traffic is expected. A basic example of how you can use Wireshark in assessing your security is to capture traffic while you log into an application and then confirm that your account credentials are not visible in the captured traffic.
Use Wireshark to analyze and ARP scan of the local network.
Instructions
1. In your terminal enter the following to start Wireshark:
wireshark &
The & starts Wireshark in the background so that you can continue to use the terminal while Wireshark is running.

2. In the Wireshark window, double-click eth0 from the list of interfaces to select it for analysis:

![](https://github.com/cybertrainingrange/Sprint-4-Anna-Francisco/assets/119987218/a7525ea8-eef4-41a5-a61f-7181b635444f)

The eth0 interface is the ethernet interface for the VM. All network traffic going outside the instance will traverse eth0.

3. In the terminal window, enter the following to generate some traffic for Wireshark to capture:
arp-scan --localnet
 
4. Enter arp in the display filter bar to display on ARP protocol traffic:
![](https://github.com/cybertrainingrange/Sprint-4-Anna-Francisco/assets/119987218/aa3703bf-d420-40b1-9b36-ba48013b48ef)
 
5. Maximize the Wireshark window and scroll to the top of the packet table at the top:
![](https://github.com/cybertrainingrange/Sprint-4-Anna-Francisco/assets/119987218/8f49c64b-4dc3-4630-8cec-7e7996194874)


Wireshark has captured all of the ARP packets that are sent by the arp-scan command. To discover hosts on the local network, arp-scan sends Who has requests to every IP in the local network address space (192.168.0.0 - 192.168.0.255). The Info column presents summaries of the requests in English. Notice the Destination column says Broadcast for the ARP request. All interfaces on the network receive broadcast requests. This enables host discovery since if there is a host on the network with the requested IP it can respond to the request to identify itself.

6. Scroll through the packets and select the one that says 192.168.0.1 is at... in the Info column:
![](https://github.com/cybertrainingrange/Sprint-4-Anna-Francisco/assets/119987218/d8e27419-029e-44d6-bc9c-745c6ae3c2e1)

This is a response to one of the ARP requests that asks who has 192.168.0.1.

 
7. In the packet details pane immediately below the packet table, click the triangle to the left of Address Resolution Protocol to expand the section:
![](https://github.com/cybertrainingrange/Sprint-4-Anna-Francisco/assets/119987218/72114214-8634-4879-b008-7d666ad66ea7">)

Wireshark understands the ARP protocol and displays the packet data in an easy to understand format. The data clearly shows the Target IP address and corresponding Target MAC address. The ARP protocol is used for determining the data link layer address (MAC address) of a given IPv4 address.
 
 
Summary

Used Wireshark to capture and analyze the traffic of a host. Specifically, you captured the traffic generated by an ARP scan and analyzed the traffic to understand what requests and responses are generated by the ARP scan.




# What is Wireshark and why is it important in cybersecurity?


Wireshark is a popular open-source network protocol analyzer. It is used for capturing and analyzing network traffic in real-time. With Wireshark, you can inspect and dissect packets of data flowing over a network, allowing you to gain deep insights into network behavior and troubleshoot network issues. It is widely used in the field of cybersecurity for several reasons:

1. Network Traffic Analysis: Wireshark provides a comprehensive view of network traffic, allowing cybersecurity professionals to analyze the behavior of network protocols, identify anomalies, and detect potential security threats or vulnerabilities. By examining packet-level details, they can understand how different network services and applications interact and uncover any suspicious or unauthorized activities.
2.  Intrusion Detection and Prevention: Wireshark can be used as part of an intrusion detection system (IDS) or intrusion prevention system (IPS) to monitor network traffic and identify potential attacks. By capturing and analyzing packets, security analysts can detect unusual patterns, suspicious activities, or known attack signatures, enabling them to respond promptly to threats.
3.   Vulnerability Analysis: Wireshark helps in identifying vulnerabilities in network configurations or application protocols. By examining packet captures, cybersecurity professionals can spot insecure practices, misconfigurations, or weak encryption methods. This information can be used to enhance the security posture by patching vulnerabilities and implementing secure network practices.
4. Malware Analysis: Wireshark can aid in the analysis of network-based malware infections. By examining the traffic generated by infected systems, security analysts can observe communication patterns, identify command-and-control servers, extract malicious payloads, and understand the behavior of the malware. This information can be crucial in developing mitigation strategies and improving defenses against similar threats.
5. Network Troubleshooting: Wireshark is an invaluable tool for diagnosing and troubleshooting network issues. By capturing packets and analyzing their contents, administrators can pinpoint problems such as misconfigurations, faulty devices, or network congestion. Wireshark's extensive filtering and search capabilities allow for efficient debugging and resolution of network-related problems.
6. Education and Research: Wireshark is widely used in cybersecurity education and research. Its user-friendly interface, extensive protocol support, and powerful analysis features make it a valuable tool for learning network protocols, conducting experiments, and conducting research on network behavior and security.


Overall, Wireshark is an essential tool in the field of cybersecurity, providing deep visibility into network traffic, aiding in the detection of security threats, assisting in vulnerability analysis, and facilitating network troubleshooting. Its versatility and extensive feature set make it a fundamental component of any cybersecurity professional's toolkit.





## Technical Documentation

[Step by step documentation](https://docs.google.com/document/d/1NVgH-7--tss2UUAKXhJSTr5uJXF0gu2p/edit#heading=h.wkfehcu9nic)

## Presentation

[Software_Documentation/Powerpoint](https://docs.google.com/presentation/d/1RJ81B93NVuC5kgsNs93FxmTOvVkBWT1XH_3W0fseMC8/edit#slide=id.g4dfce81f19_0_45)


## Agile Framework
[Jira ](https://files.slack.com/files-pri/T03MH73HJAE-F058KULNKN2/sprint_4__jira.png)



## Research Questions

[Research](https://docs.google.com/document/d/1AqU58VM01r7sKaOqERSSKUDaavQwCmAgEe6TDmCtmpQ/edit)



## Youtube Resources 

[Wireshark for beginners](https://www.youtube.com/watch?v=TkCSr30UojM)

[Wireshark](https://www.wireshark.org/)

[Intro to traffic analysis](https://www.youtube.com/watch?v=5PKAa6TI82U)

[Reading PCAP](https://www.youtube.com/watch?v=ZNS115MPsO0)

[Basics of Network analysis](https://www.youtube.com/watch?v=o-QNMSPbOGY)

## Team Members
- Anna [@annitamaria](https://github.com/orgs/cybertrainingrange/people/ANNITAMARIA)
- Francisco [@killbay](https://github.com/orgs/cybertrainingrange/people/killbay)


