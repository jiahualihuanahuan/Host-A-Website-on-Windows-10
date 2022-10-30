# Host-A-Website-on-Windows-10-
document how to host a website on a Windows 10 machine

## Install XAMPP
1. Go to https://www.apachefriends.org/
2. Download the version that suit your operating system
3. Install XAMPP


## Configuration file change to enable ssl certificate
<VirtualHost _default_:443>


## How to set a static IP address

1. Go to Control Panel -> Network and Internet -> Network and Sharing Center ->Change adapter settings
2. Select the adapter you are currently using (e.g. Ethernet or Wi-Fi) -> right click ->Properties
3. Double click on Internet Protocol Version 4 (TCP/IPv4)
4. Select Use the following IP address:
IP address: 192.168.0.14

Subnet mask: 255.255.255.0

Default gateway: 192.168.0.1

(some of the information above can be obtained from Status or ipconfig command)






