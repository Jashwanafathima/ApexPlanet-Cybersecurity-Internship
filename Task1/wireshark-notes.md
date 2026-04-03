### Wireshark Notes

**What is Wireshark?**
Wireshark is a network packet analyzer used to capture and inspect data traveling across a network.

**Steps Performed:**

1. Opened Wireshark in Kali Linux.
2. Selected the network interface (eth0).
3. Started packet capture.
4. Generated traffic using the ping command.
5. Applied filter: `icmp`

**Observations:**

* ICMP packets (Echo Request and Echo Reply) were captured.
* Source and destination IP addresses were visible.
* Communication between Kali Linux and Metasploitable2 was confirmed.

**Conclusion:**
Wireshark helps in analyzing network traffic and understanding communication between systems.

**Learning Outcome:**
Learned how to capture and filter packets using Wireshark.
