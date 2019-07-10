# Exercises week 4

1. What are the main topics we have discussed so far?
We have discussed basic network terminology. We talked about Network reconnaissance and toools. Open source recon, Host and service discovery and nmap.

Muddled points are how to analyze network reconnaissance.

# mudddled points
how would a network administrator identify a router was set up?

2. Why don't you think we hear about ddos atacks anymore?
Because they are so common, and they are resolved quickly.

3. What's the purpos of a DNS 
DNS translates ip addresses to human readable text. This helps so that people can more easily access services without the need to remember a string of numbers.

4. Assuming your browser has never been to the internet what are the steps in terms of dns that occur when you visit a site.
Your computer sends out a dns a request. To a dns resolver which points to a root server. The root server responds with the Top Level Doman Server which responds with an IP address  to the domain name server.  A dns server looks up the domain and  translates it to an ip address of the website requested.

5. How can an attacker poison the DNS attacker?
You can do it locally by doing a mitm on someones computer to upload a new dns cache. If you gain access to nytimes can poison their dns server using the same method.

You can spoof dns header.
You can reply faster than dns.
