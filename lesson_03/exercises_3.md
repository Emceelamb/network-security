1. What are the six steps of Network Recon Methodology
* Open source intelligence
* Network Discovery
* Host Discovery
* Service Discovery
* Analyze
* Goto 1

2a. What are all the possible reasons that a response is returned
1.  TCP SYN/ACK
1a. Port is open

2. TCP RST/ACK
2a. Port is closed 
2b. Firewall is blocking port

3. ICMP unreachable
3a. Firewall is rejecting packet
3b. There is a problem with the network

4. No response
4a. Firewall is dropping packet
4b. Network issue. Send multiple packets to see if its a network problem

2. What information can be returned from an nmap SYN scan?
A SYN scan can return a syn/ack which means its an open port. It can return a RST packet which means that port is closed. Or an ICMP not reachable which meanst is filtered. Finally no response which also means that it is filtered.

Exercise B. How does diagram change if the bystanders port is closed?
Innocent bystander sends a RST packet to the  victim. Victim sends no response, so the TCP SYN/Ack ip id is only x+1

3. What are possible responses to a tcp syn scan?
* RST packet
* no response
* ICMP unreachable

udp?
* returns a udp packet 
* no response 

4. Suppose you're a security engineer for a large network.
1. look up secure configuration guide.
2. update regularly and lock settings. Continuously check for configurations

5. How easy is it to spoof your IP address and send a message?
1. It is easy to change your IP address, because they are often dynamic. Hard to get the target to reply though.

Muddled point:
You mentioned that in week 2 that you didn't reveal yourself to NYU that you were scanning them. Is it beccause you used third party websites instead of applications directly on your computer?
