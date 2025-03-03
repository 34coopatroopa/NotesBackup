[[Cpre 230 Exam 1]]
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