# network mapping and port scanning
 
 | network mapping | port scanning   |
 | --------------- | --------------- |
 | dns info        | host            |
 | ping            | ports           |
 | traceroute      | services        |
 | firewalking     | vulnerabilities |

## network mapping
  ### nslookup/ dig
	 - disable unauthorized access to dns server
	 - remove unnecessary config info
	 - enable secure zone transfer
	 - split dns
  ### ping
	block icmp
  ### traceroute
	filter icmp time exceededdd
  ### firewalk
	 - discovery
	 - scanning
  ### defense
- Good security policy 
- Split DNS 
	- All public systems in one DNS server located in DMZ 
	- All internal systems using private addresses with separate DNS server internally 
- Drop/reject packets with a TTL of 1 or 0 (stop traceroute) 
- More strict ICMP rules 
	- Block incoming ICMP messages at Internet gateway to make ping ineffective 
	- Filter ICMP Time Exceeded messages leaving your network to make traceroute ineffective 
- Minimal ports open 
- Stateful inspection firewalls 
- Modified kernels/IDS to look for fingerprint packets

## port scanning
### tcp syn scan
sends rst after receiving ack
stealthy
### tcp full connection (vanilla) scan
attempts a full connection with all ports
not stealthy because connection can be logged
### tcp ack scan
can test firewall to see what types of connections it will let through
### tcp window scan
much the same as an ack scan
### ftp