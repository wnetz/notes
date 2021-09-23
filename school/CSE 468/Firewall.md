# Firewall
## Perimeter
most common type
![[perimeter firewall.png]]
![[perimeter firewall 2.png]]

## Distributed
only works if all of the firewalls are the same. otherwise a packet could get thorough on an alternate route
![[Distributed firewall.png]]

## Micro-Segmentation
came from cloud processing
![[micro-segmentation.png]]

## Architecture
### Single-Box
all are relatively economic solutions

#### Screening Router
used in packet filtering firewalls
can only decide on the information in the packet
they can be hard to manage and hare to detect  breaches
![[Screening Router.png]]

#### Dual-Homed Host
no external packets reach the inside of the network and services are provided by proxy or by logging into the dual-home host
![[Dual-Homed Host.png]]

#### Multiple-Purpose Boxes
shares both advantages and disadvantages of screening router [[#Screening Router]] and [[#Dual-Homed Host]]
![[Multiple-Purpose Boxes.png]]

### Screened Host
has both a [[#Screening Router]] and a [[#Bastion Host]]
the screening router provides the packet filtering 
the bastion host is the only thing on the internal network that allows connection to the internet
this provides better security and usability than [[#Dual-Homed Host]]
![[Screened Host.png]]

### Bastion Host
basically is a proxy and is the public face of the network
multiple bastions an be used to share load
bastions are made to be simple and limit unnecessary accesses
always be prepared to be compromised
![[Bastion Host.png]]

### Screened Subnet
adds a DMZ (demilitarized zone) to a [[#Screened Host]] to further isolate the network
moves the [[#Bastion Host]] into the DMZ
![[Screened Subnet.png]]

#### Exterior Router
allow almost anything outbound, and do very little filtering
special rules to protect the host on the perimeter net

#### Interior Router
allows selected services

## Design