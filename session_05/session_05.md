#Session 5


## persistence
How to maintain access?
* Startup service
  * linux inetd
  * windows startup key
  * cron job
* Trojan
  * a program that does something unexpected 
* virus
  * attaches itself to another program
* worm
  * similar to virus but self replicating
* blended threat
  * similar to both
* **malware** - all unauthorized software
* wrappers - how trojans get on machine

TCP/UDP Ports used by trojans
* UDP only responds 1 per second

Determining which ports are listening
* Windows
  * netstat -an
* linux
  * netstat - anp
  * lsof -i

## Proxy Server trojan
* starts hidden http proxy on victims computer
* metasploit meterpreter can easily install a proxy trojan
* netbus trojan
  * remote control program
* rootkits
  * designed to evade forensics
  * two types: User mode and Kernel mode

## Netcat
* turns network port into file
* can read/write
* make network socket like a port
* client mode/ listen mode

## Steganography
* Covert message
  * send message within another message
  * VPN
* Network Steganography
  * tunneling 
  * socks tunnel
  * ssh tunnel
  * **Hide traffic through another channel**

## TCP Header
* source port is set by sender
* sender sends sequence number
* some flags can be set

### Loki2
Loki can be used to change ICMP packet
* anything can be sent in ICMP packet

## covert\_tcp
* IP ID method- hide data in IP identification
* SEQ # method - stored in initial sequence number
* ACk # method - 
  
## reverse www shell
* covert tunnel using http

## Altering logs to hide the evidence
* better to alter log than to del log
* winzapper
* unix logger are in ascii text

## Hidden services

## Operation aurora

WHOIS is about registration information for domain
DNS 





