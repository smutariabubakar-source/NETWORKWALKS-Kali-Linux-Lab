NETWORKWALKS 
KALI-LINUX NETWORK CONFIGURATION LAB
       PROJECT OVERVIEW
This project documents the setup and network configuration of Kali Linux Virtual Machine using Oracle VirtualBox.
       OBJECTIVES
Download and install 7-zip
Download and install VirtualBox on laptop/PC
Configure the network settings on VirtualBox (create NATNetwork in 10.0.0.0/24)
Download and import Kali Linux Virtual Machine in VirtualBox
Setup the IP configuration of Kali Linux
Perform basic network discovery using Nmap.
Take snapshot of the VM

      VIRTUALBOX NETWORK CONFIGURATION
    Setting           Configuration
Virtual Machine     Kali Linux 2026.2
Network Type        NAT Network
Network Name        Kali-NAT
IPv4 Network        10.0.0.0/24
DHCP                Enabled
Kali IP Address     10.0.0.3/24
Default Gateway     10.0.0.1

  IP CONFIGURATION
The Kali network interface was configured successfully
Interface : eth0
IP Address : 10.0.0.3/24
Network : 10.0.0.0/24
Gateway : 10.0.0.1

  VERIFICATION
Check IP address
ip -4 addr show eth0
The result confimmed:
inet 10.0.0.3./24
Check routing
ip route
The result confirmed:
default via 10.0.0.1 dev eth0 10.0.0.0/24 dev eth0
Test the gateway
ping -c 4  10.0.0.1.   The Kali VM successfully received replies from the gateway.  Test Internet connectivity
ping -c 4  8.8.8.8
DNS resolution and connectivity were successful
ping -c 4 google.com
Network discovery
nmap -sn 10.0.0.0/24, for host discovery on the private lab network.

VM Snapshot
VirtualBox snapshot was created after completing the network configuration.  
Snapshot Name:  Networkkwalks - IP Configuration Complete and, to show evidence screenshots will be added to document.

   Conclusion:
Kali Linux virtual machine was successfully configured on a private NAT Network, where the VM received the IP address 10.0.0.3/24, used 10.0.0.1 as its default gateway, successfully connected to the Internet, resolved DNS names, and completed a basic Nmap host-discovery scan.
The project provided practical experience with VirtualBox, Linux networking, IP addressing, DHCP, routing, connectivity testing, and basic network discovery.




