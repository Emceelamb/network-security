HMAC uses asymmetric key and encryption uses a digital signature.
3 ways
1. Encrypt then HMAC (Protects decryption engine)
   * you encrypt the message first then HMAC
2. HMAC then encrypt (What ssl uses)
   * take hmac of plain text
   * then encrypt entire thing
   * hosts decrypts ciphertext first then check integrity
   * resource intensive
3. Encrypt and HMAC
   * only encrypts plain text

Record layer format
TLS is made of 4 layer types
* Header
  * Content Type
    * changeCipherSpec
    * Alert
    * handshaeke
    * application data

HTTPS is HTTP over TLS

Breaks content into 64kb
TLS compressions is never used.
* huge number of attacks on compression
* adds hmac
* encrypts
* then adds ssl header

SSL Handshake protocol

SSL vulnerabilities:
- Revocation is not commonly checked
- use of poor ciphers
- no infrastructure to enforce 
- physical attack
0 improper validation of cert fields
- user error
- tls renegotiaion vulnerability ( <= ssl 3.0);
- bleichenbacher attack
- ssl strip

Man in the middle attacks: 
- installing malicious root CA in user's certifcate store
- since there is a different root of trust

# Layer 2 Security
Once you're on layer 2 of network you can do everything.

* ARP is map of MAC and IP address
* MAC Address CAM Table
* CAM table is map of MAC and Port 
* cam table is physical object
* cam overflow attack
  * fails to open
  * sends to everywhere

Counter measure:

* Port security

## VLAN hopping
* VLAN is logical separation of a network.
* allows multiple networks to operate like they are on one network.
* native vlan is default
* switch spoofing
* double encapulation

## DHCP attack (DORA)
protocol used to obtaining ip addr
* DHCP function: 
* DHCP discover (broadcast)  \> "I want an IP addr"
* DHCP Offer \<  "Here is one. do you want it?" (Could be multiple offers from different servers)
* DHCP request \> "I want THIS IP addr" (all dhcp implementations chose the first one received)
* DHCP ack \< "OK, you have this ip addr"

Two attacks associated with this: 
* Rogue server
  * when another computer on network pretends to be DHCP server 
  * Gobber is name of tool to do this
* DHCP gets
  * IP
  * subnet mask
  * default router (How to get out of the network)
  * DNS server
  * lease time

* DHCP starvation attack
  * DHCP is limited to only about 1-200 ip addresses
* computer requests numerous ip addresses until there are no more available addresses

### preventative measures
* DHCP starvation attack = Port security
* DHCP header has MAC addr and Client hardware addr
* DHCP only reads hardware addresses
* * Port security does not stop DHCP starvation attack *
* DHCP Snooping
  * can label interfaces as trusted v untrested
  * only correct packets are sent from interfaces
* starts DHCP snooping binding table
  * macAdd, IpAdd, Lease, TYype, VLAN, Interfaces
* checks layer 2 addr with mac addr
* block appropriate ports

## ARP attack
* ettercap (tool)
* Attacker poisons the ARP tables
* Set computer as router
* all traffic flows through attacker

### prevention
* Dynamic ARP Inspection (DAI)
* requires dhcp snooping binding


## Spoofing attacking
Really easy to spoof IP and MAC addresses

IP Source Guard (IPSG)
* looks at every packet
* expensive (uses a lot of cpu)
* only works up to a limit of traffic

## Spanning tree protocol
* 
-


1. What is MI, PKI, TLS?
1. MI is message integrity or CIA - confidentiality, integrity, availability.
PKI is public key infrastructure. TLS is next version of SSL
2. Are there any muddled points on MI, PKI, and TLS.
2. 

3. Why is spoofing packets Layer 2 or Layer so easy?
3. Having a lot of security checks at the lower layers would be slow.

4. Why might not all orgs implement Port Security?
4. Limits number of mac addresses.
Port security only allows for 1 MAC address per interface.

5. Describe DHCP attacks
5. An attacker can be a rogue DHCP server where they pretend to be a dhcp server. This allows them to do change DNS server, and Default router. A DHCP starvation attack requests many ip addresses preventing legitimate users from obtaining ip.

6. How easy it to spoof your Mac addr? IP? Easy easy.

A. I am a little confused about 
