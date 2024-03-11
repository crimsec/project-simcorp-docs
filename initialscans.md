# Initial Scans

## Network Enumeration and Host Discovery

This is the command we used to conduct initial discovery:
> sudo nmap -v -sS -p- 10.0.0.0/24 -e tun0 --excludefile excludefile.txt -oA host-discovery

These are the full results of the initial discovery scan above:
 Nmap 7.94SVN scan initiated Mon Mar 11 13:06:24 2024 as: nmap -sn -e tun0 --excludefile /home/kali/final/exclude -oN /home/kali/final/scan_results.txt 10.0.0.0/24
Nmap scan report for 10.0.0.74
Host is up (0.054s latency).
Nmap scan report for 10.0.0.82
Host is up (0.044s latency).
Nmap scan report for 10.0.0.123
Host is up (0.059s latency).
Nmap scan report for 10.0.0.126
Host is up (0.059s latency).
Nmap scan report for 10.0.0.175
Host is up (0.048s latency).
Nmap scan report for 10.0.0.197
Host is up (0.054s latency).
 Nmap done at Mon Mar 11 13:06:44 2024 -- 249 IP addresses (6 hosts up) scanned in 19.78 seconds


## Host-specific -sV scans (Recon)

### 10.0.0.74

 Nmap 7.94SVN scan initiated Mon Mar 11 13:28:44 2024 as: nmap -sV -version-all -A -p- -oA 74-scan-results 10.0.0.74
Nmap scan report for 10.0.0.74
Host is up (0.048s latency).
Not shown: 65518 closed tcp ports (conn-refused)
PORT      STATE SERVICE            VERSION
135/tcp   open  msrpc              Microsoft Windows RPC
139/tcp   open  netbios-ssn        Microsoft Windows netbios-ssn
445/tcp   open  microsoft-ds       Windows 7 Professional 7601 Service Pack 1 microsoft-ds (workgroup: WORKGROUP)
554/tcp   open  rtsp?
2869/tcp  open  http               Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
3389/tcp  open  ssl/ms-wbt-server?
|_ssl-date: 2024-03-11T17:37:15+00:00; -8s from scanner time.
| rdp-ntlm-info: 
|   Target_Name: RISK-ANALYST1
|   NetBIOS_Domain_Name: RISK-ANALYST1
|   NetBIOS_Computer_Name: RISK-ANALYST1
|   DNS_Domain_Name: RISK-ANALYST1
|   DNS_Computer_Name: RISK-ANALYST1
|   Product_Version: 6.1.7601
|_  System_Time: 2024-03-11T17:36:08+00:00
| ssl-cert: Subject: commonName=RISK-ANALYST1
| Not valid before: 2024-03-06T18:10:19
|_Not valid after:  2024-09-05T18:10:19
5357/tcp  open  http               Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-server-header: Microsoft-HTTPAPI/2.0
|_http-title: Service Unavailable
5985/tcp  open  http               Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-title: Not Found
|_http-server-header: Microsoft-HTTPAPI/2.0
8089/tcp  open  ssl/http           Splunkd httpd
|_http-title: splunkd
| ssl-cert: Subject: commonName=SplunkServerDefaultCert/organizationName=SplunkUser
| Not valid before: 2021-06-09T20:57:41
|_Not valid after:  2024-06-08T20:57:41
|_http-server-header: Splunkd
| http-robots.txt: 1 disallowed entry 
|_/
10243/tcp open  http               Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-server-header: Microsoft-HTTPAPI/2.0
|_http-title: Not Found
47001/tcp open  http               Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-server-header: Microsoft-HTTPAPI/2.0
|_http-title: Not Found
49152/tcp open  msrpc              Microsoft Windows RPC
49153/tcp open  msrpc              Microsoft Windows RPC
49154/tcp open  msrpc              Microsoft Windows RPC
49155/tcp open  msrpc              Microsoft Windows RPC
49165/tcp open  msrpc              Microsoft Windows RPC
49168/tcp open  msrpc              Microsoft Windows RPC
Service Info: Host: RISK-ANALYST1; OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
|_clock-skew: mean: 1h23m52s, deviation: 3h07m51s, median: -8s
| smb-os-discovery: 
|   OS: Windows 7 Professional 7601 Service Pack 1 (Windows 7 Professional 6.1)
|   OS CPE: cpe:/o:microsoft:windows_7::sp1:professional
|   Computer name: RISK-ANALYST1
|   NetBIOS computer name: RISK-ANALYST1\x00
|   Workgroup: WORKGROUP\x00
|_  System time: 2024-03-11T10:36:09-07:00
| smb-security-mode: 
|   account_used: guest
|   authentication_level: user
|   challenge_response: supported
|_  message_signing: disabled (dangerous, but default)
|_nbstat: NetBIOS name: RISK-ANALYST1, NetBIOS user: <unknown>, NetBIOS MAC: 06:64:07:5b:75:69 (unknown)
| smb2-security-mode: 
|   2:1:0: 
|_    Message signing enabled but not required
| smb2-time: 
|   date: 2024-03-11T17:36:09
|_  start_date: 2024-03-07T18:10:11

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
 Nmap done at Mon Mar 11 13:37:30 2024 -- 1 IP address (1 host up) scanned in 526.40 seconds


### 10.0.0.126

 Nmap 7.94 scan initiated Mon Mar 11 13:42:40 2024 as: nmap -sV -version-all -A -p- -oA 74-scan-results 10.0.0.126
Nmap scan report for 10.0.0.126
Host is up (0.052s latency).
Not shown: 65520 closed tcp ports (conn-refused)
PORT      STATE SERVICE       VERSION
135/tcp   open  msrpc         Microsoft Windows RPC
139/tcp   open  netbios-ssn   Microsoft Windows netbios-ssn
445/tcp   open  DDcr          Windows Server 2019 Standard Evaluation 17763 microsoft-ds
3389/tcp  open  ms-wbt-server Microsoft Terminal Services
|_ssl-date: 2024-03-11T17:44:32+00:00; -2s from scanner time.
| ssl-cert: Subject: commonName=accounting1
| Not valid before: 2024-03-06T18:10:28
|_Not valid after:  2024-09-05T18:10:28
| rdp-ntlm-info: 
|   Target_Name: ACCOUNTING1
|   NetBIOS_Domain_Name: ACCOUNTING1
|   NetBIOS_Computer_Name: ACCOUNTING1
|   DNS_Domain_Name: accounting1
|   DNS_Computer_Name: accounting1
|   Product_Version: 10.0.17763
|_  System_Time: 2024-03-11T17:44:28+00:00
5985/tcp  open  http          Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-title: Not Found
|_http-server-header: Microsoft-HTTPAPI/2.0
8089/tcp  open  ssl/http      Splunkd httpd
|_http-title: splunkd
| ssl-cert: Subject: commonName=SplunkServerDefaultCert/organizationName=SplunkUser
| Not valid before: 2024-03-10T04:03:46
|_Not valid after:  2027-03-10T04:03:46
| http-robots.txt: 1 disallowed entry 
|_/
|_http-server-header: Splunkd
47001/tcp open  http          Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-server-header: Microsoft-HTTPAPI/2.0
|_http-title: Not Found
49664/tcp open  msrpc         Microsoft Windows RPC
49665/tcp open  msrpc         Microsoft Windows RPC
49666/tcp open  msrpc         Microsoft Windows RPC
49667/tcp open  msrpc         Microsoft Windows RPC
49669/tcp open  msrpc         Microsoft Windows RPC
49673/tcp open  msrpc         Microsoft Windows RPC
49674/tcp open  msrpc         Microsoft Windows RPC
49685/tcp open  msrpc         Microsoft Windows RPC
Service Info: OSs: Windows, Windows Server 2008 R2 - 2012; CPE: cpe:/o:microsoft:windows

Host script results:
| smb2-time: 
|   date: 2024-03-11T17:44:28
|_  start_date: N/A
| smb-security-mode: 
|   account_used: guest
|   authentication_level: user
|   challenge_response: supported
|_  message_signing: disabled (dangerous, but default)
|_nbstat: NetBIOS name: ACCOUNTING1, NetBIOS user: <unknown>, NetBIOS MAC: 06:11:cb:9e:24:37 (unknown)
|_clock-skew: mean: 1h23m58s, deviation: 3h07m50s, median: -2s
| smb-os-discovery: 
|   OS: Windows Server 2019 Standard Evaluation 17763 (Windows Server 2019 Standard Evaluation 6.3)
|   Computer name: accounting1
|   NetBIOS computer name: ACCOUNTING1\x00
|   Workgroup: WORKGROUP\x00
|_  System time: 2024-03-11T10:44:28-07:00
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled but not required

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
 Nmap done at Mon Mar 11 13:44:34 2024 -- 1 IP address (1 host up) scanned in 114.78 seconds

### 10.0.0.175

 Nmap 7.94SVN scan initiated Mon Mar 11 14:15:33 2024 as: nmap -sV -version-all -A -p- -oA 175-scan-results 10.0.0.175
Nmap scan report for 10.0.0.175
Host is up (0.11s latency).
Not shown: 65532 closed tcp ports (conn-refused)
PORT     STATE SERVICE  VERSION
22/tcp   open  ssh      OpenSSH 8.2p1 Ubuntu 4ubuntu0.2 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   3072 ee:5a:9a:76:38:ca:54:b6:23:18:34:96:af:15:2d:f7 (RSA)
|   256 bf:fe:e9:bb:45:ae:97:cb:25:01:23:7a:a5:34:4b:74 (ECDSA)
|_  256 9f:da:a0:0c:38:6a:97:a3:ee:b3:17:e4:7b:ef:7a:7a (ED25519)
80/tcp   open  http     Apache httpd 2.4.41 ((Ubuntu))
|_http-title: Document
|_http-server-header: Apache/2.4.41 (Ubuntu)
8089/tcp open  ssl/http Splunkd httpd
|_http-server-header: Splunkd
| http-robots.txt: 1 disallowed entry 
|_/
| ssl-cert: Subject: commonName=SplunkServerDefaultCert/organizationName=SplunkUser
| Not valid before: 2021-06-08T20:26:34
|_Not valid after:  2024-06-07T20:26:34
|_http-title: splunkd
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
 Nmap done at Mon Mar 11 14:24:09 2024 -- 1 IP address (1 host up) scanned in 515.92 seconds


### 10.0.0.197

 Nmap 7.94SVN scan initiated Mon Mar 11 13:40:25 2024 as: nmap -sV -version-all -A -p- -oA 197-scan-results 10.0.0.197
Nmap scan report for 10.0.0.197
Host is up (0.040s latency).
Not shown: 65520 closed tcp ports (conn-refused)
PORT      STATE SERVICE       VERSION
135/tcp   open  msrpc         Microsoft Windows RPC
139/tcp   open  netbios-ssn   Microsoft Windows netbios-ssn
445/tcp   open  microsoft-ds  Windows Server 2019 Standard Evaluation 17763 microsoft-ds
3389/tcp  open  ms-wbt-server Microsoft Terminal Services
| ssl-cert: Subject: commonName=accounting2
| Not valid before: 2024-03-06T18:10:01
|_Not valid after:  2024-09-05T18:10:01
| rdp-ntlm-info: 
|   Target_Name: ACCOUNTING2
|   NetBIOS_Domain_Name: ACCOUNTING2
|   NetBIOS_Computer_Name: ACCOUNTING2
|   DNS_Domain_Name: accounting2
|   DNS_Computer_Name: accounting2
|   Product_Version: 10.0.17763
|_  System_Time: 2024-03-11T17:42:19+00:00
|_ssl-date: 2024-03-11T17:42:27+00:00; -1s from scanner time.
5985/tcp  open  http          Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-title: Not Found
|_http-server-header: Microsoft-HTTPAPI/2.0
8089/tcp  open  ssl/http      Splunkd httpd
|_http-title: splunkd
| http-robots.txt: 1 disallowed entry 
|_/
|_http-server-header: Splunkd
| ssl-cert: Subject: commonName=SplunkServerDefaultCert/organizationName=SplunkUser
| Not valid before: 2024-03-11T02:04:13
|_Not valid after:  2027-03-11T02:04:13
47001/tcp open  http          Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-title: Not Found
|_http-server-header: Microsoft-HTTPAPI/2.0
49664/tcp open  msrpc         Microsoft Windows RPC
49665/tcp open  msrpc         Microsoft Windows RPC
49666/tcp open  msrpc         Microsoft Windows RPC
49667/tcp open  msrpc         Microsoft Windows RPC
49669/tcp open  msrpc         Microsoft Windows RPC
49670/tcp open  msrpc         Microsoft Windows RPC
49674/tcp open  msrpc         Microsoft Windows RPC
49685/tcp open  msrpc         Microsoft Windows RPC
Service Info: OSs: Windows, Windows Server 2008 R2 - 2012; CPE: cpe:/o:microsoft:windows

Host script results:
|_nbstat: NetBIOS name: ACCOUNTING2, NetBIOS user: <unknown>, NetBIOS MAC: 06:d7:72:ae:fb:51 (unknown)
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled but not required
| smb-security-mode: 
|   account_used: <blank>
|   authentication_level: user
|   challenge_response: supported
|_  message_signing: disabled (dangerous, but default)
| smb-os-discovery: 
|   OS: Windows Server 2019 Standard Evaluation 17763 (Windows Server 2019 Standard Evaluation 6.3)
|   Computer name: accounting2
|   NetBIOS computer name: ACCOUNTING2\x00
|   Workgroup: WORKGROUP\x00
|_  System time: 2024-03-11T10:42:19-07:00
| smb2-time: 
|   date: 2024-03-11T17:42:19
|_  start_date: N/A
|_clock-skew: mean: 1h23m59s, deviation: 3h07m50s, median: -1s

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
 Nmap done at Mon Mar 11 13:42:28 2024 -- 1 IP address (1 host up) scanned in 122.48 seconds
