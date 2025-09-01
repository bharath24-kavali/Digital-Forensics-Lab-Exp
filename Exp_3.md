# Exprement_3: Capture and Analyze Network Traffic using Wireshark
## Aim and Description
The primary aim of using Wireshark is to capture and analyze data packets traveling over a computer network. This process, often called packet sniffing or network analysis, allows you to inspect the raw data of network communication. It's used for troubleshooting network problems, analyzing application performance, and understanding network protocols. Wireshark is a free, open-source network protocol analyzer that's widely used by network administrators, security professionals, and developers.
![alt text](<screenshorts/Exp_3/Screenshot (14).png>)
## Tools and Equipment
Computer: A desktop or laptop with a working network interface card (NIC).

Wireshark: The software application, which you can download for free from the official Wireshark website.

Network Connection: An active internet or local network connection (Ethernet or Wi-Fi).

Target Network: The network you want to monitor. It could be your local network or a specific part of a larger network.
![alt text](<screenshorts/Exp_3/Screenshot (15).png>)
## Procedure
Capturing and analyzing network traffic with Wireshark is a straightforward process, but it requires careful steps to ensure you capture the right data.

Launch Wireshark: Open the Wireshark application. You'll be presented with a list of available network interfaces (e.g., Ethernet, Wi-Fi).

Select an Interface: Choose the network interface you want to monitor. A live graph next to the interface name helps you identify the one with active traffic.

Start Capturing: Double-click the desired interface or select it and click the Start capturing packets button (the fin icon) to begin the capture.

Generate Traffic: Perform the network activity you want to analyze. For example, open a web browser and visit a website, or run an application that communicates over the network.

Stop Capturing: Once you've captured enough data, click the Stop capturing packets button (the red square icon).

Analyze the Captured Data:

Filter Traffic: Use the filter bar at the top to narrow down the captured packets. For example, type http to see only HTTP traffic or ip.addr == 192.168.1.10 to view traffic to and from a specific IP address.

Inspect Packets: Click on a packet in the top pane to see its details in the middle and bottom panes. The middle pane shows the protocol layers (e.g., Ethernet, IP, TCP) and the bottom pane displays the raw hexadecimal and ASCII data of the packet.
![alt text](<screenshorts/Exp_3/Screenshot (17).png>)
## Result
Upon completion, you will have a detailed record of the network communication that occurred during the capture period. Key results include:

Packet List: A chronological list of all captured packets, showing the time, source and destination IP addresses, protocol, and a brief description.

Packet Details: A structured view of a selected packet, breaking it down by protocol layers, which helps you understand how the data is encapsulated.

Packet Bytes: A raw view of the packet's data, which can be useful for low-level analysis or forensic examination.
![alt text](<screenshorts/Exp_3/Screenshot (18).png>)
Statistical Analysis: Wireshark also provides various statistics, such as protocol hierarchy, endpoint lists, and conversation graphs, to help you visualize and summarize the captured data.