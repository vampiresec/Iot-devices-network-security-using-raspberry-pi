# Iot-devices-network-security-using-raspberry-pi
IoT makes ordinary items' smart 'by allowing them, without needing any human
interference, to relay data and automate tasks. An IoT device may be as basic as a portable
health monitoring device, or as difficult as a smart city with sensors in all its regions. Due
to IoT a huge data is transferred over the internet. Cyber-crime and attacks are on the rise
these days, making security a basic prerequisite as well as a need. As any form of internet
communication and data storage grows more dangerous, it's critical to keep our home
network up to date in terms of security, minimising loopholes, and ensuring data integrity
and incorruptibility. When properly designed, intrusion detection systems and honeypots
can provide useful solutions. For total network monitoring and security, the performance
of a Raspberry Pi module running an IDS (Intrusion Detection System), a packet analyzer,
and a decoy server called honeypot will be employed. It will help to capture the attacker as
well as a weak secured system in the network.


# Requirements

1. [Snort](https://www.snort.org/downloads) 
2. Tshark 
3. [Cowrie](https://github.com/cowrie/cowrie) 
4. [Barnyard2](https://github.com/firnsy/barnyard2)
5. [Pulledpork](https://github.com/shirkdog/pulledpork)
6. nmap
7. Hydra

# Configuration
### Tshark
    sudo tshark
### Snort commands
    sudo snort -A console -q -u snort -g snort -c /etc/snort/snort.conf -i <inteface>

### Cowrie
```
sudo adduser --disabled-password cowrie
```
```
sudo su - cowrie
```
```
cd cowrie
```
```
source cowrie-env/bin/activate
```
```
pip install --upgrade pip
```
```
pip install --upgrade -r requirements.txt
```
```
nano etc/cowrie.cfg
```
```
  [telnet]
  enabled = true
```
```
bin/cowrie start
```

Port redirection commands are system-wide and need to be executed as root. A firewall redirect can make your existing SSH server unreachable, remember to move the existing server to a different 

The following firewall rule will forward incoming traffic on port 22 to port 2222 on Linux:

```
sudo iptables -t nat -A PREROUTING -p tcp --dport 22 -j REDIRECT --to-port 2222
```
Or for telnet:
```
sudo iptables -t nat -A PREROUTING -p tcp --dport 23 -j REDIRECT --to-port 2223
```
# Testing
* Cowrie<br>
    test the honeyport by bruteforcing the telnet service
    ```
    brute-force telnet service with command hydra -l pi -P worldlist -s 2223 <raspberry_pi_ip> telnet
    ```
* Snort<br>
    ping raspberrypi
    ```
    ping <raspberry_pi_ip>
    ```
