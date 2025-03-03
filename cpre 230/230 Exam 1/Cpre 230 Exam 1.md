## 1. Basics of IP Addressing and Subnetting

1. **Understanding Binary and Decimal Representations of IP Addresses**
    
    - Converting IP addresses between binary and decimal.
    - Relevance of dotted-decimal notation.
2. **CIDR Notation and Subnet Masks**
    
    - How CIDR (/24, /16, etc.) translates into subnet masks (255.255.255.0, etc.).
    - The concept of network portion vs. host portion in an IP address.
3. **Network Address and Broadcast Address Calculation**
    
    - How to derive the network address from an IP and a subnet mask.
    - How to derive the broadcast address.
    - Example: 89.55.174.15/24 → Network address, broadcast address.
4. **Loopback Address**
    
    - Purpose of 127.0.0.1 and its role in testing local TCP/IP stack.

---

## 2. Basic Networking Services and Protocols

1. **DNS (Domain Name System)**
    
    - Forward lookups (resolving a domain name to an IP).
    - Reverse lookups (resolving an IP to a domain name).
2. **Connection-Oriented vs. Connectionless Protocols**
    
    - Definition of connection-oriented protocols (e.g., TCP).
    - Contrast with connectionless protocols (e.g., UDP).
3. **Password Storage Best Practices**
    
    - Why passwords should be hashed + salted in a database.
    - Common hashing algorithms and their strengths/weaknesses.

---

## 3. Basic Linux Commands (Command-Line Focus)

1. **IP Address and Network Interface Commands**
    
    - `ifconfig` or `ip addr show` to display the IP address of a network interface.
    - Checking your LAN card interface details (eth0, etc.).
2. **Routing Table Display**
    
    - `route -n` or `ip route show` to display the current routing table.
3. **Testing Network Connectivity**
    
    - Using `ping` (ICMP echo requests) to check connectivity to remote hosts.
4. **Editing System Configuration Files**
    
    - Opening files (e.g., `/etc/hosts`) with a console text editor like `vi`, `nano`.
5. **Basic Firewalling with iptables**
    
    - Understanding the default policies (ACCEPT, DROP).
    - Adding rules to block or allow traffic (e.g., webserver traffic, blocking pings).

---

## 4. Routing and Network Design

1. **Understanding the Routing Table**
    
    - How routes are matched (longest-prefix match).
    - The meaning of destination, gateway, mask, interface.
2. **Adding/Modifying Routes**
    
    - Commands like `route add`, `ip route add` to configure static routes.
    - Determining which network interface or gateway to use for a given destination.
3. **iptables for Packet Filtering**
    
    - The difference between INPUT, OUTPUT, FORWARD chains.
    - Writing rules to block or allow ICMP/pings.
    - Example: blocking all pings to/from a given network (e.g., 6.6.6.0/24).
4. **Network Diagrams and Multi-Router Environments**
    
    - Identifying how many IP networks exist.
    - Routing table entries for multiple routers.
    - Directly connected networks vs. learned routes.

---

## 5. Packet Analysis (tcpdump / Wireshark Concepts)

1. **Reading Basic Packet Captures**
    
    - Understand how to read source/destination IP addresses in a capture (e.g., packet 48 vs. packet 50).
    - Broadcast vs. unicast packets—who “receives” them.
2. **Address Resolution**
    
    - How a broadcast or multicast packet can target multiple machines.
    - The concept of ARP (Address Resolution Protocol) and “who gets the packet.”
3. **Following a Connection**
    
    - Identifying the source IP, destination IP, and whether a protocol is using broadcast/multicast vs. unicast.
    - Understanding how an IP might change after initial negotiations (DHCP, NAT scenarios, etc. — though not specifically mentioned, it’s good background knowledge).

---

## 6. Putting It All Together

1. **Practical Exercises**
    
    - Practice calculating network/broadcast addresses for various IP/CIDR combos.
    - Practice writing out a small network diagram, labeling IP addresses, and constructing minimal routing tables.
    - Practice iptables commands to allow/deny traffic, focusing on pings or HTTP (webserver) traffic.
2. **Exam-Style Questions**
    
    - Work through short-answer questions about DNS vs. loopback addresses.
    - Configure or interpret routing rules for a multi-interface scenario.
    - Write iptables commands to block or permit traffic based on address ranges.

---

### Recommended Study Sequence Summary

1. **IP Addressing, Subnetting, Loopback**
2. **DNS, Protocols (TCP vs. UDP), Password Storage**
3. **Linux Networking Commands (ip/ifconfig, ping, route, opening files)**
4. **Routing (tables, adding routes) & iptables basics**
5. **Packet Capture Interpretation**
6. **Practical Application & Synthesis (working with exam-style questions)**