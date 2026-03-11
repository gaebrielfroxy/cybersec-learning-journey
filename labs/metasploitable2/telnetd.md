#Metasploitable Recon

Target: 192.168.56.101

## Port Scan
nmap -sS T4 192.168.56.101

Open ports discovered:
21/tcp   open  ftp  
22/tcp   open  ssh  
23/tcp   open  telnet 
25/tcp   open  smtp  
53/tcp   open  domain  
80/tcp   open  http  
111/tcp  open  rpcbind  
139/tcp  open  netbios-ssn  
445/tcp  open  microsoft-ds  
512/tcp  open  exec  
513/tcp  open  login  
514/tcp  open  shell  
1099/tcp open  rmiregistry  
1524/tcp open  ingreslock  
2049/tcp open  nfs  
2121/tcp open  ccproxy-ftp  
3306/tcp open  mysql  
5432/tcp open  postgresql  
5900/tcp open  vnc  
6000/tcp open  X11  
6667/tcp open  irc  
8009/tcp open  ajp13  
8180/tcp open  unknown  

## Service Detection

Command:
nmap -sV 192.168.56.101 -v

Key findings:
port 21 ftp service: vsftpdf 2.3.4

## Enumeration

FTP
- login msfadmin/msfadmin works
- files accessible

Telnet
- not tested yet

HTTP
- web interface available

MySQL
- not tested

## Research
Command:
searchsploit telnetd

Result:
xploit Title                             |  Path
------------------------------------------- ---------------------------------
netkit-telnet-0.17 telnetd (Fedora 31) - ' | linux/remote/48170.py
TelnetD encrypt_keyid - Function Pointer O | linux/remote/18280.c
------------------------------------------- ---------------------------------
------------------------------------------- ---------------------------------
 Shellcode Title                           |  Path
------------------------------------------- ---------------------------------
Linux/MIPS (Little Endian) - system(telnet | linux_mips/27132.txt


## Exploitation:

Exploit used:
telnetd

Command:
telnet 192.168.56.101 23 
login with: msfadmin/msfadmin

Result:
Command shell obtained

## Lessons learned

Not every exploit from searchsploit works - always check service version 




