# Network

## Scanning Tools

Get devices connected to same network (IPv4):  
`arp-scan --interface=eth0 --localnet`

Get hostname by IP:  
`host xx.x.x.xx`

`Zenmap` is a GUI for `nmap`.  
Nmap can be used for network scans like `nmap -F -T4 XX.XX.XX.XX` for a
scan only checking the 100 most important ports from `/usr/share/nmap/nmap-services`
and doing that very fast (timing schema 4).

As a wlan network scanner `netdiscover` can be used.

`p0f` is nice to use to not be detected, since it does not start any traffic itself.

To list smb servers `sbmtree` can be used.

## Login Cracker

`hydra` supports many protocols to do parallelized dictionary attacks. Protocols are for example FTP, HTTP(S), IMAP, MySQL, Microsoft SQL, POP3, PostgresSQL, SMTP, Telnet, VNC. Also there is support to "fill" web forms (GET, PUT, POST).  
Hydra has to be fed with a password list (dictionary).

## Misconfiguration

`nikto` tries to call known paths for systems and lists their vulnerability if found.  
For example `nikto -h github.com -p 80,443 -o out.txt` will check for vulnerabilities
on github for port 80 and 443 and add the output to out.txt.
