# Penetration Introduction

## Network

### Tools

#### Macchanger

##### Installation:

```
$ sudo pacman -S macchanger
``` 

##### Basic Usage:

```
$ macchanger -r interface //change to random mac address
$ macchanger --mac=XX:XX:XX:XX:XX:XX interface //choose specific
$ macchanger -p interface //change back to permanent hardware mac
```

#### SHIP

Ship is a tool to collect and map some data about address and ports

##### Installation:

```
$ pacman -S gawk grep iproute2 mtr iputils sed traceroute wget
$ git clone https://github.com/xtonousou/ship.git
```

##### Basic Usage:

```
$ ship.sh //start program (or create symlink)
$ ship -i //show interfaces
```

There are many other options like [-g] for gateway, [-4|-6] for ipv4/ipv6, [-H] for host, [-HM] for host and mac address, [-e <url>] for the ip of an url, [-c <ip>] to calculate from an IP, or to do port listening [-p <port number>].
  
#### Wireshark

#### Tcpdump

#### Nmap

#### Aircrack-ng
