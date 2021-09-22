# Addresses
- types of addresses
	- physical
		- #MAC_Address
		- directly points to neighbor
	- logical
		- #IP
		- source and destination
	- port
		- #TCP
		- #UDP
		- #port_number
		- identifies the application to send and receive packet
	- specific
		- process ID

## MAC Address
#MAC_Address 

- 48 bits 6 byte 12 hex
- needs to be changed when forwarding to next network segment

## IP Address
#IP/v4 
![[The IPv4 Header.png]]
#IP/v6
![[The IPv6 Header.png]]

all 0's is reserved for the network address, and all 1's is reserved for broadcast

### class full IP Addressing 
is very inefficient for many networks
class A /8
class B /16
class C /24

### Private IP Addresses
10.0.0.0/8 			  1 class A
127.16.0.0/12 		16 class B
192.168.0.0/16	  256 class C


## ports
#port_number
#Transport_Layer 
- 16 bit integer (0 `rir:ArrowRight`  65,535)
- servers use 0-1023