#  `ip link` command
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
