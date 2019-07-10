# Lesson 03
## Network Attack Methodology
* Recon
* Scanning
* Vulnerability Identification
* Exploitation
* Post Exploitation

## Recap
* Brute force forward dns
  * lookup subdomains/ associated domains
  * possibly misconfigured/ vulnerable

* Split DNS
  * way external and internal dns are implemented
  * Look for misconfigurations

## Port scanning

### TCP 3-way handshake
 _____ _____ TCP SYN ____  ____
|ALICE|-- TCP SYN/ ACK ---|NYU|
 ----- --- TCP ACK ----   ----_

### 1. TCP  3-way handshake (port is open)
| ACK TYPE | Source Port | Destination Port |
|----------|-------------|------------------|
| TCP SYN  | x > 1023    | 80               |
| TCP SYN/ACK| 80 | x > 1023 |
| TCP ACK | x > 1023 | 80 |

* Source port is randomy generated number
  * usuall 10k+

### 2. TCP 3-way handshake (port is closed) 
| ACK TYPE | Source Port | Destination Port |
|----------|-------------|------------------|
| TCP SYN  | x > 1023    | 80 (HTTP)        |
| TCP RST/ACK| 80 | x > 1023 |

* You get a reset packet
* RST = RESET

### 3. TCP 3-way handshake (Firewall "rejects" packet)
 _____ _____ TCP SYN ____  ____
|ALICE|--ICMP Unreachable--|NYU|
 -----                    ----_
* Reject is a response

### 4. TCP 3-way handshake (no response)
 _____ _____ TCP SYN ____  ____
|ALICE|--------------------|NYU|
 -----  No response        ----_
 * Firewall is dropping packet
 * no response

## Possible responseces to TCP SYN packet on a report
1. TCP SYN/ACK
2. TCP ST/ ACK
3. ICMP unreachable
4. No response

What are all the possible reasons that a response is returned
1.  TCP SYN/ACK
1a. Port is open
 
2. TCP RST/ACK
2a. Port is closed 
2b. Firewall is blocking port

3. ICMP unreachable
3a. Firewall is rejecting packet
b. There is a problem with the network
 
4. No response
a. Firewall is dropping packet
b. Network issue. Send multiple packets to see if its a network problem

### TCP ACK Scan (with no prior comm)
* **Normal** - returns rst packet
* **Firewall** - typical response is nothing

### TCP SYN PACKET first (dest port 80)
* **Normal** - RST return
* **TCP Ack** (src port 80)
  * ICMP unreachable (nothing) *rare*
* This means there is a firewall

> TCP ACKs are not helpful when used without another scan type. If no response it means that a firewall makes port 80 closed. Port 80 may be running behind a firewall

## Firewalls work with port numbers and IP addr

## NMAP
* **TCP CONNECT**
  * Most reliable
  * Open ports reply with SYN/ACK
  * Closed ports reply with /RST/ACK
  * TCP SYN -> TCP SYN/ACK <- TCP ACK -> TCP FIN -> TCP FIN/ACK <-
  * At least 5 packets
  * uses OS API
* **TCP SYN** (half open scan)
  * Stealthy
  * *much* faster
  * Max 3 packets
  * TCP SYN -> TCP SYN/ACK <- TCP RST ->
* **TCP FIN**
  * should return RST packet 
  * mostly works on UNIX devices
* **TCP NULL**
  * sends a packet with no flags
  * OS responds differently
* **TCP ACK**

## UDP Scan
* much simpler than TCP
* connetionless
* less reliable/ a response is not assured
* slower scanning

### possible responses to UDP packet
* Open some ICMP response
  * UDP request response is UDP
* Closed 
  * ICMP unreachable
* Open/ filtered
  * No response
    * packet got dropped?
    * service not responding (improperly formatted packet)
    * firewall is blocking
* DNS is a popular UDP
* DHCPD is a UDP packet
* UDP returns only one packet per second
* scanning udp is hard to scan
  * because its slow
  * must be properly formatted to
* UDP can be used to bypass security

 > ACK Scanning is to check for firewalls

## FTP bounce scan
* scans for anonymous FTP
  * port scan data from an anon FTP

### IP Packet
![Ip packet datagram](http://mars.netanya.ac.il/~unesco/cdrom/booklet/HTML/NETWORKING/IMAGES/ipheader.gif)
* IP IDs should be random

## IDLE Scan
* scan feature of nmap to "Frame" another computer
* takes IP address of another machine and uses it to spoof a SYN scan

## useful nmap flags
- `-sV` propes open ports to determinse service 
- `-o` enable OS detection
- `-sC` enable script scnning
- `-T4` sets template for fast scans
- `-oA` output file

## Firewalk
* like traceroute for application data

## httprecon
* web server fingerprinting

## vega
* web app vulnerability check


