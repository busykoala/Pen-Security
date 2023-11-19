# Network attacking tooling

## burpsuite

Traffic intercepting, changing payloads on the fly and much much more.

## sqlmap

Inject sql payloads.

## hydra

`hydra` supports many protocols to do parallelized dictionary attacks. Protocols are for example FTP, HTTP(S), IMAP, MySQL, Microsoft SQL, POP3, PostgresSQL, SMTP, Telnet, VNC. Also there is support to "fill" web forms (GET, PUT, POST).  
Hydra has to be fed with a password list (dictionary).

## macchanger

```bash
# shut interface down
ip link set dev <interface> down

# do stuff with mac addr
macchanger -r <interface>  # change to random mac address
macchanger --mac=XX:XX:XX:XX:XX:XX <interface>  # choose specific
macchanger -p <interface>  # change back to permanent hardware mac

# take interface up again
ip link set dev <interface> up
```

## aircrack-ng

```bash
sudo airmon-ng start interface  # put interface into monitor mode (mon0)
airodump-ng mon0  # list access point (AP) info
airodump-ng -c yy --bssid xx:xx:xx:xx:xx:xx -w dump_file mon0  # yy chanel, xx:xx... mac

# if successfull it will list bssid and station
aireplay-ng -0 2 -a BB:BB:BB:BB:BB:BB -c AA:AA:AA:AA:AA:AA mon0  # force deauth

# BB number BSSID, AA number STATION, -0 deauth attack, 2 n-try
aircrack-ng dump_file -w password.dict  # brute force handshake
airmon-ng stop wlan0mon  # return to managed mode
```

## SHIP

Ship is a tool to collect and map some data about address and ports

- [ship repo](https://github.com/xtonousou/ship.git)

```bash
ship.sh  # start program (or create symlink)
ship -i  # show interfaces
```

There are many other options like `-g` for gateway, `-4|-6` for ipv4/ipv6, `-H` for host, `-HM` for host and mac address, `-e <url>` for the ip of an url, `-c <ip>` to calculate from an IP, or to do port listening `-p <port number>`.
