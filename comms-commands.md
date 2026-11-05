#  `ip link show` command
```
# show all network interfaces
ip link show

# show specific interface
ip link show <interface name>
Example: ip link show eth0

# show interface statistics
ip -s link show <interface name>
Example: ip -s link show eth0
```

# `ip addr show` command
```
# show ip address of all interfaces
ip add show

# show ip of a specific interface
ip addr show <interface name>
```

# `ip route show` command
```
# show routing table
ip route show

# show all routing tables
ip route show table all
```

# `ip neigh show` command
```
# show neighbors
ip neigh show
```

#  `tcpdump` command
```
# Basic Capture (for example ntp packets)
tcpdump -nni any udp port 123
where -nn (don not resolve hostname and portname) and -i (interface)

# filtering by protocols
<udp/tcp/icmp> etc.

# saving and reading captures
## capture/saving
tcpdump -w capture.pcap
## reading from pcap file
tcpdump -r capture.pcap


```
