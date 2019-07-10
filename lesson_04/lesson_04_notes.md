# Lesson 04
## Exploitation

By using third party resources you can hide your activities from network administrator. Not foolproof. Admins can request info from ISP or website  owners, etc.

## IP addr spoofing
* You can only spoof in one direction

## Filtering
* 127.x is internal ip address
* ingress filtering - filter traffic coming into network (inbound)
* local network > regional isp > tier 1 isp
* you can apply ingress filtering as close to endpoint
  * however it requires proper setup or else you will be blocking wrong people
* egress filtering - filterr traffice exiting network (outbound)

## Session hijacking
* Neet to knows
  * 1. spoof IP
  * 2. get correct sequence number


## SYN floods
* SYN receive/ack and does nothing
* server is waiting
* creates an open port
* can send many syn packets from different IPs/ports so the server is waiting for times X 
* Size of TCP SYN Packet = IP header + TCP header size = 20b + 20b = 40b very small
* form of DDOS attack

### SYN cookies
* server sends a TCP SYN/ACK with a cookie or Initial sequence number
 
## DNS 

## DNS attack: (DNS cache poisoning)
* dns has no authentication
* can redirect the domain to another ip address
* your browser has no method of showing

## Nessus

# Scan all ports





