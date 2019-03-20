## About

This repository is thought as a reference, introduction and collection of tools and methods to penetrate.
The tools probably work on most linux distros but are here shown for Arch.

## Table of Contents

1. [Network](#network)
  - [Macchanger](#macchanger)
  - [SHIP](#ship)
  
2. [Database](#database)
3. [Webseites](#websites)
4. [Forensics](#forensics)
5. [Cryptography](#cryptography)
6. [Reverse Engineering](#reverse-engineering)
7. [Binaries and Files](#binaries-and-files)
  - [Binwalk](#binwalk)

## Network

### Macchanger

#### Installation

```
$ sudo pacman -S macchanger
``` 

#### Usage

```
$ macchanger -r interface //change to random mac address
$ macchanger --mac=XX:XX:XX:XX:XX:XX interface //choose specific
$ macchanger -p interface //change back to permanent hardware mac
```

### SHIP

Ship is a tool to collect and map some data about address and ports

#### Installation

```
$ pacman -S gawk grep iproute2 mtr iputils sed traceroute wget
$ git clone https://github.com/xtonousou/ship.git
```

#### Usage

```
$ ship.sh //start program (or create symlink)
$ ship -i //show interfaces
```

There are many other options like `-g` for gateway, `-4|-6` for ipv4/ipv6, `-H` for host, `-HM` for host and mac address, `-e <url>` for the ip of an url, `-c <ip>` to calculate from an IP, or to do port listening `-p <port number>`.
  
### Wireshark

### Tcpdump

### Nmap

### Aircrack-ng

## Database

## Webseites

## Forensics

## Cryptography

## Reverse Engineering

## Binaries and Files

### Binwalk

#### Installation
```
$ sudo pacman -S binwalk
```
#### Usage
```
$ binwalk file //show files in file
$ binwalk -e file //extract files in file
```





