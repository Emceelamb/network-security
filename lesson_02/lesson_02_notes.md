# Lesson 02
## Readings

* [Attack Trees](https://www.schneier.com/paper-attacktrees-ddj-ft.html "schneier attack trees")
* [10 Techniques for Blindly Mapping Internal Networks](https://blog.netspi.com/10-techniques-for-blindly-mapping-internal-networks/ "map internal networks")
* [TCP IDLE Scan](http://nmap.org/book/idlescan.html "nmap")
* [Security Issues with DNS (Page 2-8 only)](http://www.sans.org/reading-room/whitepapers/dns/security-issues-with-dns-1069 "sans.org dns")
* [Firewalk : Can Attackers See Through Your Firewall?](http://www.giac.org/paper/gsec/312/firewalk-attackers-firewall/100588 "firewalk")
* [Missed Alarms and 40 Million Stolen Credit Card Numbers: How Target Blew It](http://www.bloomberg.com/bw/articles/2014-03-13/target-missed-alarms-in-epic-hack-of-credit-card-data "bloomberg")
* [Windows 7, not XP, was the reason last week’s WCry worm spread so widely](https://arstechnica.com/security/2017/05/windows-7-not-xp-was-the-reason-last-weeks-wcry-worm-spread-so-widely/ "ars technica")

### Background Information

* [How the Domain Name System (DNS) Works](https://www.verisign.com/en_US/website-presence/online/how-dns-works/index.xhtml "DNS")
* [TCP Connection Establishment Process: The "Three-Way Handshake](http://www.tcpipguide.com/free/t_TCPConnectionEstablishmentProcessTheThreeWayHandsh-3.htm "tcp auth")
* [Google Hacking: What is a Google Hack?](https://www.acunetix.com/websitesecurity/google-hacking/ "google hacking")
* [What is DHCP and how does it work?](https://www.grandmetric.com/2017/07/18/what-is-dhcp-and-how-does-it-work/ "dhcp")
* [Cryptography - A General Overview](http://adeptus-mechanicus.com/codex/gencrypt/gencrypt.html "crypt")
* [Address Resolution Protocol Tutorial, How ARP work, ARP Message Format](http://www.omnisecu.com/tcpip/address-resolution-protocol-arp.php "arp")
* [IP Addressing and Subnetting for New Users](https://www.cisco.com/c/en/us/support/docs/ip/routing-information-protocol-rip/13788-3.html "IP")
* [Computer Network | Network address translation (NAT)](https://www.geeksforgeeks.org/computer-network-network-address-translation-nat/ "NAT")


## Attack trees

* Attackers are lazy
* Create a tree of necessary steps
  * assign attributes to each step
  * impossible/ possible
  * costs 
* You can also use an and/ or flow chart

## Network Reconnaissance
* DNS 
* WHOIS
* Headers
* Port scanning 
* nmap

## Types of attacks
* ddos
* destruction
* emanation eavesdropping - signal eaves dropping
* information warfare AKA "fake news"

## 6 steps of Network Recon
1. Collect Public Information
2. Network Dicovery
3. Host Discovery
4. Service  Discovery
5. Service Discovery
6. Recursion

### What info we are looking for?
* IP address
* Network Topology
* Domain Names
* user acct names
* OS/ software being used
* Security policy
* Physical security system
* Home address of employees
* Frequent hangouts of employees

## Collect public information
* Change caller id
* Asterisk server - free and open source spoofing sofware

### Google search
* `site:` searches only within given domain
  * `site:poly.edu keyword`
* `link:` shows all sites linked to the specific site 
  * `link:www.poly.edu keyword`
* `intitle:` shows pages whose title matches search criteria
* `inurl:` shows pages with in url 
* `related:` shows similar pages
* [Exploit DB](https://www.exploit-db.com/google-hacking-database/ "google hacking website")  

### Maltego










































