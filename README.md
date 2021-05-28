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

### Snort commands
    sudo snort -A console -q -u snort -g snort -c /etc/snort/snort.conf -i inteface

### Cowrie
'''
sudo adduser --disabled-password cowrie<br>

'''
'''
sudo adduser --disabled-password cowrie<br>
'''

'''

'''

'''

'''

'''

'''


    
    
    sudo su - cowrie
    git clone http://github.com/cowrie/cowrie
4. cd cowrie
5. source cowrie-env/bin/activate
6. pip install --upgrade pip
7. pip install --upgrade -r requirements.txt
8. nano etc/cowrie.cfg
   \[telnet\]
  enabled = true
