# Networking

```bash
# list network interfaces
ip link show
netstat -i
tcpdump --list-interfaces

# scan devices connected to same network (IPv4)
arp-scan --interface=<interface> --localnet
netdiscover

# get ip by host
host <host>
nslookup <host>
# get host by ip
host <ip>
nslookup <ip>

# check common ports from "/usr/share/nmap/nmap-services"
nmap -F -T4 <ip>
nmap <ip> -p80-82
nc -vz <ip> <port>

# some more discovery commands
dig @<custom-dns> <domain> TXT
ping <ip>
whois <host>

# get network hops
traceroute <ip>
mtr <ip>

# URL scan
nikto -h <URL> -p 80,443 -o results.txt  # https://github.com/sullo/nikto

# capture network traffic
tcpdump -i <interface> -s 65535 -w capture.pcap  # analyze with wireshark
p0f -i <interface> -o capture.txt  # passive, doesn't start any traffic itself

# analyze ssl certs
openssl s_client \
    -connect <host>:443 \
    -servername <host> </dev/null 2>/dev/null | openssl x509 -noout -text

# get listening tcp/udp info
netstat -tulpn
ss -tulpn
```
