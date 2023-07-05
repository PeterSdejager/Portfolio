# eJPT Study Guide

### Background

#### The eLearnSecurity Junior Penetration Tester (eJPT) is a 100% practical certification on penetration testing and information security essentials. By passing the exam, a cyber security professional proves to employers they are ready for a rewarding new career. - [https://elearnsecurity.com/product/ejpt-certification/](https://elearnsecurity.com/product/ejpt-certification/)

### Cheat Sheet

* `ping <IP>`
  * to see if you have access to a device/system at an IP Address
* `ip addr`
  * Identify the IP address of the **your** Kali Instance.
* `route`
  * check the routing table on the instance
* `ip route add 192.168.222.0/24 via 10.175.34.1`
  * manually add a route to the routing table
  * "Add a route to 192.168.222.0/24 through the 10.175.34.1 IP Address"
  * For our case, the gateway/router was 10.175.34.1
* `fping -a -g 192.168.82.0 192.168.82.255 2>/dev/null`
  * See hosts that are alive/up
  * To suppress the messages of offline hosts
* `nmap -sn 192.168.10.0/16`
  * ping scan
* `nmap -sT -sS -sV <target(s)>`
  * `-sT` -> TCP connect scan
  * `-sS` -> SYN scan / stealth scan
  * `-sV` -> version detection scan
* `nmap --script=ftp* 192.168.0.10 -p 21`
  * all FTP-related scripts including `ftp-brute`
* `sqlmap -u <URL> -p <injection parameter> [options]`
  * SQLMap basic syntax
* `nbstat -A <IP>`
  * Windows command for enumerating Windows shares
  * `<00>` - Workstation
  * `UNIQUE` - computer must have one IP assigned to it
  * `<20>` - file sharing service is up and running
* `smbclient -L //<IP> -N`
  * FTP-like client to access Windows shares
  * `-L` -> see what services are available on target
  * `-N` -> not to ask for password
* `enum4linux -U -o 192.168.1.200`
  * PERL script similar to _enum_ and _Winfo_
* (On Meterpreter) `run autoroute -s 192.179.47.2 -n 255.255.255.0`
  * `-s` -> the IP you are trying to reach
  * `-n` -> subnet mask
  * helpful when you do not have access to a network but your webshell has access to it
* Nessus
  * Helps automate finding alive hosts and their vulnerabilities
* `gobuster dir -u <IP or website> -w <wordlist>`
  * directory bruteforce tool
  * `feroxbuster`, `dirbuster`, `dirb` are also good alternatives
* `hashcat -m <mode> <hash file> <wordlist>`
  * [https://hashcat.net/wiki/doku.php?id=example\_hashes](https://hashcat.net/wiki/doku.php?id=example\_hashes)

### Tips & Tricks

* I think `fping -a -g 192.168.10.0/24 2>/dev/null` - `nmap -sn 192.168.10.0/24` gives you the routers on the network
  * fping shows all alive devices, while nmap shows only alive hosts (excluding routers)
  * So, 10 devices in fping and 8 hosts in nmap = 2 routers on the scanned network
  * THIS IS A THEORY
* If you do not have direct access to an IP use `autoroute` in msfconsole. If you have access through a router use `ip route add .....`
  * After you get `autoroute` to work, you can use `use auxiliary/scanner/portscan/tcp` to then scan the IP Addresses you have just routed to see the open ports on them.
* If there are multiple Metaploit exploits for one vulnerability, try all of them.

### Resources I used while studying

[https://github.com/JasonTurley/eJPT/blob/main/cheat-sheet.md\
https://bhavsec.com/posts/ejpt-cheatsheet/\
https://github.com/tejasanerao/eJPT-Cheatsheet\
https://pjdeepakkumar.gitbook.io/ejpt-cheet-sheet/\
https://www.marabellisec.com/certifications/pass-the-ejpt-cheat-sheet\
https://kentosec.com/2019/08/04/how-to-pass-the-ejpt/\
http://alexwpryor.com/certification-reviews/my-ejpt-review/\
https://www.reddit.com/r/eJPT/comments/o1oimt/ejpt\_100\_just\_passed/\
https://www.reddit.com/r/eJPT/comments/px7sgc/just\_passed\_the\_ejpt\_some\_thoughtsconcerns/\
https://github.com/navisk13/eJPT-resources\
https://www.reddit.com/r/eLearnSecurity/comments/lp286m/pivoting\_resources\_cheatsheet/\
https://pentest.blog/explore-hidden-networks-with-double-pivoting/\
https://guide.offsecnewbie.com/cherrytree-oscp-template\
https://github.com/CountablyInfinite/oscp\_cheatsheet\
https://www.offensive-security.com/metasploit-unleashed/portfwd/](https://github.com/JasonTurley/eJPT/blob/main/cheat-sheet.mdhttps://bhavsec.com/posts/ejpt-cheatsheet/https://github.com/tejasanerao/eJPT-Cheatsheethttps:/pjdeepakkumar.gitbook.io/ejpt-cheet-sheet/https://www.marabellisec.com/certifications/pass-the-ejpt-cheat-sheethttps://kentosec.com/2019/08/04/how-to-pass-the-ejpt/http://alexwpryor.com/certification-reviews/my-ejpt-review/https://www.reddit.com/r/eJPT/comments/o1oimt/ejpt\_100\_just\_passed/https://www.reddit.com/r/eJPT/comments/px7sgc/just\_passed\_the\_ejpt\_some\_thoughtsconcerns/https://github.com/navisk13/eJPT-resourceshttps://www.reddit.com/r/eLearnSecurity/comments/lp286m/pivoting\_resources\_cheatsheet/https://pentest.blog/explore-hidden-networks-with-double-pivoting/https://guide.offsecnewbie.com/cherrytree-oscp-templatehttps://github.com/CountablyInfinite/oscp\_cheatsheethttps:/www.offensive-security.com/metasploit-unleashed/portfwd/)
