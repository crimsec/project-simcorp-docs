# Nmap 7.94SVN scan initiated Mon Mar 11 14:32:42 2024 as: nmap -sV --script=vulscan/vulscan.nse -oA 175-vulscan 10.0.0.175
Nmap scan report for 10.0.0.175
Host is up (0.10s latency).
Not shown: 997 closed tcp ports (conn-refused)
PORT     STATE SERVICE  VERSION
22/tcp   open  ssh      OpenSSH 8.2p1 Ubuntu 4ubuntu0.2 (Ubuntu Linux; protocol 2.0)
| vulscan: VulDB - https://vuldb.com:
| No findings
| 
| MITRE CVE - https://cve.mitre.org:
| No findings
| 
| SecurityFocus - https://www.securityfocus.com/bid/:
| No findings
| 
| IBM X-Force - https://exchange.xforce.ibmcloud.com:
| No findings
| 
| Exploit-DB - https://www.exploit-db.com:
| No findings
| 
| OpenVAS (Nessus) - http://www.openvas.org:
| No findings
| 
| SecurityTracker - https://www.securitytracker.com:
| No findings
| 
| OSVDB - http://www.osvdb.org:
| No findings
|_
80/tcp   open  http     Apache httpd 2.4.41 ((Ubuntu))
|_http-server-header: Apache/2.4.41 (Ubuntu)
| vulscan: VulDB - https://vuldb.com:
| No findings
| 
| MITRE CVE - https://cve.mitre.org:
| No findings
| 
| SecurityFocus - https://www.securityfocus.com/bid/:
| No findings
| 
| IBM X-Force - https://exchange.xforce.ibmcloud.com:
| No findings
| 
| Exploit-DB - https://www.exploit-db.com:
| No findings
| 
| OpenVAS (Nessus) - http://www.openvas.org:
| No findings
| 
| SecurityTracker - https://www.securitytracker.com:
| No findings
| 
| OSVDB - http://www.osvdb.org:
| No findings
|_
8089/tcp open  ssl/http Splunkd httpd
| vulscan: VulDB - https://vuldb.com:
| No findings
| 
| MITRE CVE - https://cve.mitre.org:
| No findings
| 
| SecurityFocus - https://www.securityfocus.com/bid/:
| No findings
| 
| IBM X-Force - https://exchange.xforce.ibmcloud.com:
| No findings
| 
| Exploit-DB - https://www.exploit-db.com:
| No findings
| 
| OpenVAS (Nessus) - http://www.openvas.org:
| No findings
| 
| SecurityTracker - https://www.securitytracker.com:
| No findings
| 
| OSVDB - http://www.osvdb.org:
| No findings
|_
|_http-server-header: Splunkd
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Mar 11 14:33:33 2024 -- 1 IP address (1 host up) scanned in 50.89 seconds
